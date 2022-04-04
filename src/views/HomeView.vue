<template>
    <component :is="view" v-bind:url="vurl" @closeViewer="view = ''"></component>
    <div class="top-section">

    </div>
    <div id="title-section" class="title-section">
        <div class="title-container">
            <h1 class="title-name">Luca Wolckenhauer</h1>
            <hr>
            <h1 class="title-desc" id="titleDesc">IT-Specialist and Programmer</h1>
        </div>
        <div class="arrow-container" v-bind:style="{display: titleArrowVisibility}">
            <img src="../assets/arrowdown.gif">
        </div>
    </div>
    <div class="main-content" v-bind:style="{display: showMainContent}">
        <div v-bind:style="{animation: this.introductionAnimation}" class="introduction-section" id="introductionSection" >
            <img class="introduction-image" src="../assets/lucawolckenhauer-cropped.jpg" v-bind:style="{animation: introductionAnimation}">
            <div class="introduction-text">
                <h1>hello im Luca, let me introduce myself!</h1>
                <p>I'm really fascinated by and into technology in general. I like to understand<br>
                how stuff works under the hood and then make something new based on this knowledge.<br>
                In my freetime i like to do stuff with my friends and watch or read thought provoking<br>
                articles and movies. I also do experiments on my raspberry pi like a live temperature website (solarflare-pi)
                or hosting a nextcloud instance via docker (<a target="_blank" href="https://cloud.wolckenhauer.net">link</a>)
                </p>
            </div>
        </div>
        <div class="skill-section">
            <h1>My Skills</h1>
            <div class="skill-container">
                <div class="skilltree">
                    <h1>languages</h1>
                    <div class="skill">
                        <img src="../assets/cpp-icon.png">
                        <p>C++</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/python-icon.png">
                        <p>Python</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/javascript-icon.png">
                        <p>JavaScript</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/typescript-icon.png">
                        <p>TypeScript</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/html5-icon.png">
                        <p>HTML</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/css-icon.png">
                        <p>CSS</p>
                    </div>
                </div>
                <div class="skilltree">
                    <h1>software</h1>
                    <div class="skill">
                        <img src="../assets/linux-icon.png">
                        <p>Linux</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/windows-icon.png">
                        <p>Windows</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/msoffice-icon.png">
                        <p>Microsoft Office</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/vmware-icon.png">
                        <p>VMWare</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/docker-icon.png">
                        <p>Docker</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/vscode-icon.png">
                        <p>VS Code</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/git-icon.png">
                        <p>Git</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/cisco-icon.png">
                        <p>Cisco IOS</p>
                    </div>
                </div>
                <div class="skilltree">
                    <h1>frameworks</h1>
                    <div class="skill">
                        <img src="../assets/vuejs-icon.png">
                        <p>VueJS</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/electron-icon.png">
                        <p>Electron</p>
                    </div>
                    <div class="skill">
                        <img src="../assets/express-icon.png">
                        <p>ExpressJS</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="project-section">
            <h1>Personal Projects</h1>
            <div class="project-container">
                <div class="project">
                    <div class="project-title">
                        <h1>solarflare-pi</h1>
                    </div>
                    <div class="project-scene">
                        <div class="project-card">
                            <div class="project-face project-front">
                                <p>Hover</p>
                            </div>
                            <div class="project-face project-back">
                                <p>tests with websockets and temperature readers</p>
                                <video autoplay loop playsinline src="../assets/movies/solarflare-pi.webm"></video>
                                <p>
                                This Project was made out of an Raspberry Pi Nano and a Django Webserver. The Website
                                shows the live temperature of an sensor connected to the pi. The Temperature is sent over
                                TCP from the Pi to the Webserver. <a target="_blank" href="https://github.com/CruZer0/solarflare-pi">Github Link</a>.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="project">
                    <div class="project-title">
                        <h1>peddit</h1>
                    </div>
                    <div class="project-scene">
                        <div class="project-card">
                            <div class="project-face project-front">
                                <p>Hover</p>
                            </div>
                            <div class="project-face project-back">
                                <p>a electron reddit client</p>
                                <video autoplay loop playsinline src="../assets/movies/peddit_show.webm"></video>
                                <p>
                                    This App is supposed to run on a small (max. 12 inch) Screen and
                                    Scroll your personal Reddit Home Feed. 
                                    For the authentification and API Calls there is an seperate 
                                    module called reddit-juice which i have written in TS.
                                    Right now the App is in early development and far behind the feature set
                                    it should have. Later i want to add a settings menu and add touch gestures
                                    for navigation. This is still an private repository so i can only offer an
                                    <a href="../assets/downloads/peddit-main.zip" download>Download Link</a>
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="project">
                    <div class="project-title">
                        <h1>wolckenhauerNET</h1>
                    </div>
                    <div class="project-scene">
                        <div class="project-card">
                            <div class="project-face project-front">
                                <p>Hover</p>
                            </div>
                            <div class="project-face project-back">
                                <p>Personal Website</p>
                                <video autoplay loop playsinline src="../assets/movies/lwwebsite.webm"></video>
                                <p>
                                    a website that gives me an stage to present myself. its also this very website :) 
                                    when you are interested in the source code here is the github link on behalf the <a target="_blank" href="https://github.com/CruZer0/wolckenhauer-vue">frontend</a> and here's
                                    the github link for the <a href="https://github.com/CruZer0/wolckenhauer-express" target="_blank">backend</a> .
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="certification-section">
            <h1>Certificates</h1>
            <p>In the past i completed multiple certficates. Please take a look.</p>
            <div class="certification-container">
                <div v-on:click="this.vurl = require('../assets/certificates/cisco_ccna.png'); this.view = 'imgViewer'" class="certificate">
                    <img src="../assets/cisco-ccna-white.jpg">
                    <h1>Cisco CCNA</h1>
                    <p>Click anywhere to show the certificate</p>
                </div>
                <div v-on:click="this.vurl = require('../assets/certificates/moc2074.png'); this.view = 'imgViewer'" class="certificate">
                    <img src="../assets/ms-logo-cert.png">
                    <h1>Microsoft MOC2074</h1>
                    <p>Click anywhere to show the certificate</p>
                </div>
                <div v-on:click="this.vurl = require('../assets/certificates/securepoint-utm.png'); this.view = 'imgViewer'" class="certificate">
                    <img src="../assets/securepoint_logo.jpg">
                    <h1>Securepoint UTM</h1>
                    <p>Click anywhere to show the certificate</p>
                </div>
            </div>
        </div>
        <div class="contact-section">
            <h1>Contact</h1>
            <p>If you have questions or other interests, please leave a message.</p>
            <Contact></Contact>
        </div>
        <div class="footer-section">
            <p>© Luca Wolckenhauer 2022</p>    
        </div>   
    </div>   
</template>

<script>
import ImgViewer from "../components/ImgViewer.vue"
import Contact from "../components/Contact.vue"

export default {
    name: "HomeView",
    components: {
        ImgViewer,
        Contact
    },
    data(){
        return{
            view: '',
            vurl: '',
            introductionAnimation: '',
            introductionIntersection: null,
            showMainContent: 'none',
            titleArrowVisibility: 'none',
        }
    },
    mounted(){
        this.introductionIntersection.observe(document.querySelector("#introductionSection"))
        this.checkTitleIdle()
    },
    created(){
        var introductionIteration = 0
        this.introductionIntersection = new IntersectionObserver(() => {

            if(introductionIteration > 0){
                this.introductionAnimation = "scaleDown .7s linear forwards"
            }
            else{
                introductionIteration++
            }
        }, {threshold: [0.5]})



        


    },
    methods: {
        checkIfScrolled(){
            return new Promise((resolve) => {
                window.addEventListener("scroll", () => {
                    clearTimeout(scrollTimer)
                    resolve(true)
                })
                const scrollTimer = setTimeout(() => {
                    resolve(false) 
                }, 5000)  

            })
        },
        async checkTitleIdle(){
            document.querySelector("#titleDesc").addEventListener("animationend",async () => {
                console.log("123")
                this.showMainContent = 'block'
                var didScroll = await this.checkIfScrolled()
                if(didScroll == false){
                    console.log("arrow")
                    this.titleArrowVisibility = 'block'
                    window.addEventListener("scroll", () => {
                        this.titleArrowVisibility = 'none'
                    })
                }
                
            })
        },

    }
}
</script>

<style>
    @media not screen and (max-width: 600px){
        @keyframes scaleDown {
            from{scale: 400%; opacity: 0;}
            to{scale: 100%; opacity: 1;}
        }
        @keyframes titleFadeIn {
            to{opacity: 100%;}
        }
        @keyframes titleScrollAnimation{
            from{color: white}
            to{color: red}
        }
        @keyframes titleNameMove {
            from{transform: translateX(300%);}
            to{transform: translateX(0%);}
        }
        @keyframes titleDescMove {
            from{transform: translateX(-300%); opacity: 1;}
            to{transform: translateX(0%); opacity: 1;}
        }

        .title-section{
            width: 100%;
            height: 100vh;
        }
        .title-section hr{
            width: 60%;
            color: white;
        }
        .title-container{
            display: flex;
            text-align: center;
            justify-content: center;
            align-items: center;
            animation: titleZoomOut 2s linear;
            flex-direction: column;
            height: 100%;
        }
        .title-name{
            animation: titleNameMove 1s ease-in forwards;
        }
        .title-desc{
            animation: titleDescMove 1s ease-in forwards;
            animation-delay: 1s;
            opacity: 0;
        }
        .arrow-container{
            position: absolute;
            bottom: 1%;
            left: calc(50% - 5em);
        }
        .arrow-container img{
            width: 10em;
        }
        .main-content{
            width: 60%;
            margin: auto;
        }

        .introduction-section{
            display: flex;
            align-items: flex-start;
            border: white solid 0.3em;
            border-radius: 1em;
            padding: 1em;
            overflow:hidden;
            margin-top: 1em;
            opacity: 0;
        }
        .introduction-section h1{
            padding: 0;
            margin: 0;
        }
        .introduction-image{
            min-width: 25%;
            width: 25%;
            margin-right: 3em;
        }
        .skilltree{
            display: flex;
            flex-direction: column;
            width: 100%;
            margin-right: 4em;
        }
        .skilltree img {
            width: 3em;
            align-self: center;
            margin-right: 1em;
        }
        .skill-section{
            border: white solid 0.3em;
            border-radius: 1em;
            padding: 1em;
            margin-top: 1em;
            width: 100%;
        }
        .skill-section h1{
            margin-bottom: 1em;
            text-align: center;
        }
        .skill{
            display: flex;
            font-size: 1em;
            margin-bottom: .5em;
        }
        .skill:hover{
            transform: scale(110%);
            cursor: pointer;
        }
        .skill-container{
            display: flex;
            flex-direction: row;
        }
        .project-section{
            margin-top: 1em;
            z-index: 0;
        }
        .project-container{
            display: flex;
            margin-top: 1em;
            justify-content: center;
            align-items: center;
        }
        .project{
            margin-bottom: 1em;
            margin-left: 1em;
            flex: 1;
            align-items: center;
        }
        .project-card{
            background-color: transparent;
            width: 22em;
            height: 35em;
            position: relative;
            transition: transform 0.5s;
            transform-style: preserve-3d;
            z-index: 0;
        }
        .project-scene{
            perspective: 1000px;   
        }
        .project-scene:hover .project-card{
            transform: rotateY(180deg);
        }
        .project-face{
            position: absolute;
            top: 0;
            left: 0;
            backface-visibility: hidden;
            z-index: 1;
            width: 100%;
            height: 100%;
        }

        .project-back .project-card{
            background-color: black;
        }
        .project-front{
            background-color: white;
            padding: 0;
            color: black;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .project-front p{
            text-align: center;
        }
        .project-back{
            background-color: black;
            width: 100%;
            height: 100%;
            transform: rotateY(180deg);
        }
        .project-back p{
            
        }
        .project-title{
            background-color: white;
            color: black;   
        }
        .project-title h1{
            margin: 0;
            padding: 0em 0.5em 0em 0.5em;
            font-weight: normal;
            text-align: center;
        }
        .project-back video{
            width: 100%;
        }
        .project-hidden{
            opacity: 0;
            z-index: -1;
            width: 33%; 
        }
        .certification-container{
            display: flex;
            flex-direction: row;
        }
        .certificate{
            width: 50%;
            border: 0.2em white solid;
            padding: 1em;
            margin-left: 1em;
        }
        .certificate:hover{
            transform: scale(105%);
            cursor: pointer;
        }
        .certificate img{
            width: 100%;
        }
        .contact-section{
            margin-top: 1em;
        } 
        .footer-section{
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
    @media screen and (max-width: 600px){
        @keyframes scaleDown {
            from{scale: 400%; opacity: 0;}
            to{scale: 100%; opacity: 1;}
        }
        @keyframes titleFadeIn {
            to{opacity: 100%;}
        }
        @keyframes titleScrollAnimation{
            from{color: white}
            to{color: red}
        }
        @keyframes titleNameMove {
            from{transform: translateX(300%);}
            to{transform: translateX(0%);}
        }
        @keyframes titleDescMove {
            from{transform: translateX(-300%); opacity: 1;}
            to{transform: translateX(0%); opacity: 1;}
        }

        .title-section{
            width: 100%;
            height: 100vh;
        }
        .title-section hr{
            width: 60%;
            color: white;
        }
        .title-container{
            display: flex;
            text-align: center;
            justify-content: center;
            align-items: center;
            animation: titleZoomOut 2s linear;
            flex-direction: column;
            height: 100%;
        }
        .title-name{
            animation: titleNameMove 1s ease-in forwards;
        }
        .title-desc{
            animation: titleDescMove 1s ease-in forwards;
            animation-delay: 1s;
            opacity: 0;
        }
        .arrow-container{
            position: absolute;
            bottom: 1%;
            left: calc(50% - 5em);
        }
        .arrow-container img{
            width: 10em;
        }
        .main-content{
            width: 95%;
            margin: auto;
        }

        .introduction-section{
            display: flex;
            align-items: flex-start;
            flex-direction: column;
            border: white solid 0.3em;
            border-radius: 1em;
            padding: 1em;
            overflow:hidden;
            margin-top: 1em;
            opacity: 0;
        }
        .introduction-section h1{
            padding: 0;
            margin: 0;
        }
        .introduction-image{
            width: 100%;
        }
        .skilltree{
            display: flex;
            flex-direction: column;
            width: 100%;
        }
        .skilltree img {
            width: 3em;
            align-self: center;
            margin-right: 1em;
        }
        .skill-section{
            border: white solid 0.3em;
            border-radius: 1em;
            padding: 1em;
            margin-top: 1em;
        }
        .skill-section h1{
            margin-bottom: 1em;
            text-align: center;
        }
        .skill{
            display: flex;
            font-size: 1em;
            margin-bottom: .5em;
        }
        .skill:hover{
            transform: scale(110%);
            cursor: pointer;
        }
        .skill-container{
            display: flex;
            flex-direction: column;
            width: 100%;
        }
        .project-section{
            margin-top: 1em;
            z-index: 0;
        }
        .project-container{
            display: flex;
            margin-top: 1em;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .project{
            margin-bottom: 1em;
            flex: 1;
            align-items: center;
        }
        .project-card{
            background-color: transparent;
            width: 100%;
            position: relative;
            transition: transform 0.5s;
            transform-style: preserve-3d;
            z-index: 0;
        }
        .project-front{
            display: none;
        }
        .project-back{
            width: 100%;
            height: 100%;
        }
        .project-title{
            background-color: white;
            color: black;  
            height: 100%; 
            width: 100%;
        }
        .project-title h1{
            margin: 0;
            padding: 0em 0.5em 0em 0.5em;
            font-weight: normal;
            text-align: center;
        }
        .project-back video{
            max-width: 100%;
        }
        .project-hidden{
            opacity: 0;
            z-index: -1;
            width: 33%; 
        }
        .certification-container{
            display: flex;
            flex-direction: column;
        }
        .certificate{
            border: 0.2em white solid;
            padding: 1em;
            margin-bottom: 1em;
        }
        .certificate:hover{
            transform: scale(105%);
            cursor: pointer;
        }
        .certificate img{
            width: 100%;
        }
        .contact-section{
            margin-top: 1em;
        } 
        .footer-section{
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
</style>