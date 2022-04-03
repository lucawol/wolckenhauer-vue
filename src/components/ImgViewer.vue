<template>
    <div class="viewer-container">
        <p v-on:click="closeComponent()">X</p>
    </div>
    <div class="image-container">
        <img class="image" v-bind:src="ImgURL">
    </div>


</template>

<script>
export default {
    name: "ImgViewer",
    props: ['url'],
    data(){
        return{
            ImgURL: this.url
        }
    },
    methods: {
        closeComponent(){
            this.$emit("closeViewer")
        }
    }
}
</script>

<style scoped>
@media not screen and (max-width: 600px)  {
    .image-container{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        width: 100%;
        min-height: 100%;
        position: fixed;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 5;
    }
    .image{
        max-width: 100%;
        height: 100%;

    }
    .viewer-container{
        min-height: 100%;
        min-width: 100%;
        position:fixed;
        z-index: 10;
    }
    .viewer-container p{
        font-size: 2em;
        margin: 0;
        top: 0.5em;
        left: 0.5em;
        padding-left: 0.4em;
        padding-right: 0.4em;
        position: fixed;
        border: .2em white solid;
        border-radius: 50%;
    }
    .viewer-container p:hover{
        background: grey;
        cursor: pointer;
    }
}
@media screen and (max-width: 600px)  {
    .image-container{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100vw;
        height: 100vh;
        position: fixed;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 5;
    }
    .image{
        width: 100vw;
    }
    .viewer-container{
        position:fixed;
        z-index: 10;
    }
    .viewer-container p{
        font-size: 2em;
        margin: 0;
        top: 0.5em;
        left: 0.5em;
        padding-left: 0.4em;
        padding-right: 0.4em;
        position: fixed;
        border: .2em white solid;
        border-radius: 50%;
    }
    .viewer-container p:hover{
        background: grey;
        cursor: pointer;
    }
}

</style>