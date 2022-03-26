<template>
    <div class="contact-container">
        <label for="name">name</label>
        <br>
        <input id="name">
        <br>
        <label for="email">email</label>
        <br>
        <input id="email">
        <br>
        <label for="subject">subject</label>
        <br>
        <input id="subject">
        <br>
        <label for="message">message</label>
        <br>
        <input id="message">
    </div>
</template>

<script>
export default {
    name: "Contact",
    data(){
        return{
            form: {
                name: '',
                email: '',
                
            }
        }
    }
}
</script>

<style scoped>

</style>