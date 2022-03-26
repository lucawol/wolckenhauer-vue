<template>
    <div class="pdfviewer" v-on:click="initPDFViewer()">
    </div>
</template>

<script>
import pdfjsDist from "../../node_modules/pdfjs-dist/build/pdf"

export default {
    name: "PDFViewer",
    data(){
        return {
            ViewerState: {
                pdf: null,
                currentPage: 1,
                zoom: 1
            }
        }
    },
    methods: {
        initPDFViewer(){
            pdfjsDist.getDocument("../assets/certificates/moc2074.pdf").then(pdf => {
                this.ViewerState.pdf = pdf
                console.log(pdf)
            })
        }
    }
}
</script>

<style scoped>
    .pdfviewer{
        width: 100px;
        height: 100px;
        background-color: white;
        position: sticky;
        top: calc(50% - 100px);
        left: calc(50% - 100px);
    }
</style>