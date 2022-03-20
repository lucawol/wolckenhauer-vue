<template>
    <div class="topSection">

    </div>
    <div class="titleSection">
      <h1>Luca Wolckenhauer</h1>
      <hr>
      <h1>IT-Specialist and Programmer</h1>
    </div>
    <div class="mainContent">
        <div class="introductionSection">
            <img class="introductionImage" src="../assets/lucawolckenhauer-cropped.jpg">
            <div class="introductionText">
                <h1>hello im Luca, let me introduce myself!</h1>
                <p>I'm really fascinated by and into technology in general. I like to understand<br>
                how stuff works under the hood and then make something new based on this knowledge.<br>
                In my freetime i like to do stuff with my friends and watch or read thought provoking<br>
                articles and movies. I also do experiments on my raspberry pi like a live temperature website (solarflare-pi)
                or hosting a nextcloud instance via docker (<a target="_blank" href="https://cloud.wolckenhauer.net">link</a>)
                </p>
            </div>
        </div>
        <div class="skillSection">
            <h1>My Skills</h1>
            <div class="skillContainer">
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
        <div class="projectSection">
            <h1>Projects</h1>
            <div class="projectContainer">
                <div class="project">
                    <div class="project-title">
                        <h1>solarflare-pi</h1>
                    </div>
                    <div class="project-content">
                        <p>tests with websockets and temperature readers</p>
                        <img src="../assets/solarflarepi-presentation.gif">
                        <p>
                        This Project was made out of an Raspberry Pi Nano and a Django Webserver. The Website
                        shows the live temperature of an sensor connected to the pi. The Temperature is sent over
                        TCP from the Pi to the Webserver. <a target="_blank" href="https://github.com/CruZer0/solarflare-pi">Github Link</a>.
                        </p>

                    </div>
                </div>
                <div class="project">
                    <div class="project-title">
                        <h1>peddit</h1>
                    </div>
                    <div class="project-content">
                        <p>a electron reddit client</p>
                        <img src="../assets/peddit-presentation.gif">
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
                <div class="project">
                    <div class="project-title">
                        <h1>wolckenhauerNET</h1>
                    </div>
                    <div class="project-content">
                        <p>Personal Website</p>
                        <p>
                        Its this Website :)
                        </p>
                    </div>
                </div>
            </div>
        </div>   
    </div>   
</template>

<script>
export default {
    name: "HomeView"
}
</script>

<style scoped>

  .titleSection{
    text-align: center;
    width: 100%;
  }

  .mainContent{
    width: 60%;
    margin: auto;
  }

  .titleSection hr{
    width: 60%;
    color: white;
  }
  .introductionSection{
    display: flex;
    align-items: flex-start;
    border: white solid 0.3em;
    border-radius: 1em;
    padding: 1em;
    animation-name: scaleDown;
    animation-duration: 1s;
    overflow:hidden;
  }
  .introductionSection h1{
    padding: 0;
    margin: 0;
  }
  .introductionImage{
    min-width: 25%;
    width: 25%;
    margin-right: 3em;
  }
  .skilltree{
    display: flex;
    flex-direction: column;
    margin-right: 4em;
  }
  .skilltree img {
      width: 3em;
      align-self: center;
      margin-right: 1em;
  }
  .skillSection{
      border: white solid 0.3em;
      border-radius: 1em;
      padding: 1em;
      margin-top: 1em;
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
  .skillContainer{
      display: flex;
      flex-direction: row;
  }
  .projectContainer{
      display: flex;
      flex-direction:column;
      margin-top: 1em;
  }
  .project{
        margin: auto;
      border: white solid 0.3em;
      border-radius: 1em;
      margin-bottom: 1em;
      flex: 1;
      width: 50%;
      align-items: center;
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
  .project-content{
      padding: 0.3em 0.2em 0.3em 0.2em;
  }
  .project-content img{
      max-width: 100%;
  }
  @keyframes scaleDown {
      from{scale: 400%}
      to{scale: 100%}
  }
</style>