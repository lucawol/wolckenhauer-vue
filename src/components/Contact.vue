<template>
    <div class="contact-container">
        <div v-if="success || error" class="messagebox">
            <p class="messagebox-close" v-on:click="error = ''; success = ''">X</p>
            <p>{{success || error}}</p>
        </div>
        <br>
        <label for="name">name</label>
        <br>
        <input v-model="form.name" id="name">
        <br>
        <label for="email">email</label>
        <br>
        <input v-model="form.mail" id="email">
        <br>
        <label for="subject">subject</label>
        <br>
        <input v-model="form.subject" id="subject">
        <br>
        <label for="message">message</label>
        <br>
        <textarea v-model="form.message" id="message"></textarea>
        <br>
        <button v-if="form.name && form.mail && form.subject && form.message" v-on:click="sumbitContact()">Submit</button>
        <p v-else>please fill out the form to submit the data</p>
    </div>
</template>

<script>
import axios from "axios"
export default {
    name: "Contact",
    data(){
        return{
            form: {
                name: '',
                email: '',
                subject: '',
                message: ''
            },
            error: '',
            success: ''
        }
    },
    created(){

    },
    methods: {
        async sumbitContact(){
            await axios.post('/contact', this.form)
                .then(resp => {
                    this.success = resp.statusText
                })
                .catch(err => {
                    this.error = err
                }) 
        }
    }
    
}
</script>

<style scoped>



@media not screen and (max-width: 600px) {
    .contact-container{
        margin-bottom: 10em;
        width: 30%;
    }

    .contact-container input, textarea{
        background: transparent;
        color: white;
        resize: none;
        box-sizing: border-box;
        border-radius: 0.7em;
        margin-bottom: 1em;
        padding: 0.5em;
        width: 100%;
    }

    .contact-container textarea{
        height: 10em;
    }
    .contact-container input{
        height: 2.2em;
    }

    .contact-container button{
        background: transparent;
        color:white;
        border: 0.2em white solid;
        border-radius: 0.7em;
        height: 2.2em;
    }
    .contact-container button:hover{
        color: black;
        background-color: white;
        cursor: pointer;
    }

    .messagebox{
        border: 0.2em white solid;
        border-radius: 1em;
        padding: 0.7em;
        display: flex;
    }
    .messagebox p {
        margin-right: 1em;
    }
    .messagebox-close{
        cursor: pointer;
    }
}

@media screen and (max-width: 600px) {
    .contact-container{
        margin-bottom: 10em;
        width: 100%;
    }

    .contact-container input, textarea{
        background: transparent;
        color: white;
        resize: none;
        box-sizing: border-box;
        border-radius: 0.7em;
        margin-bottom: 1em;
        padding: 0.5em;
        width: 100%;
    }

    .contact-container textarea{
        height: 10em;
    }
    .contact-container input{
        height: 2.2em;
    }

    .contact-container button{
        background: transparent;
        color:white;
        border: 0.2em white solid;
        border-radius: 0.7em;
        height: 2.2em;
    }
    .contact-container button:hover{
        color: black;
        background-color: white;
    }

    .messagebox{
        border: 0.2em white solid;
        border-radius: 1em;
        padding: 0.7em;
        display: flex;
    }
    .messagebox p {
        margin-right: 1em;
    }
    .messagebox-close{
        cursor: pointer;
    }
}

</style>