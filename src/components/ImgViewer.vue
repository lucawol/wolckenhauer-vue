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
.image-container{
    display: flex;
    align-items: center;
    justify-content: center;
    padding-bottom: 1em;
    padding-top: 1em;
    width: 100%;
    min-height: 100%;
    position: fixed;
    background-color: rgba(0, 0, 0, 0.5);
}
.image{
    z-index: 1;
    max-width: 100%;

}
.viewer-container{
    min-height: 100%;
    min-width: 100%;
    position:fixed;
    z-index: 2;
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
</style>