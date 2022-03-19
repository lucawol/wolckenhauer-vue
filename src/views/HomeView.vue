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
        <div class="skilltree">
        <h1>languages</h1>
        <ul>
          <li>C++</li>
          <li>Python</li>
          <li>JavaScript/TypeScript</li>
          <li>HTML</li>
          <li>CSS</li>
        </ul>
        </div>
        <div class="skilltree">
        <h1>software</h1>
        <ul>
          <li>Linux</li>
          <li>Windows</li> <!-- show infobox when hovering -->
          <li>VMWare</li>
          <li>Docker</li>
          <li>VS Code</li>
          <li>Git</li>
          <li></li>
        </ul>
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
  .titleSection {
    
  }

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
    float:left;
  }
</style>