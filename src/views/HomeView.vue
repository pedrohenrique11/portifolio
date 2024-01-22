<script setup>
import MyProfile from '../components/MyProfile.vue'
import TheButtons from '../components/TheButtons.vue'
import TextSection from '../components/TextSection.vue'

</script>

<template>
  <main>
    <MyProfile />
    <div>
      <TextSection 
      title='About me' 
      text="I've always been captivated by how technology is capable of changing people's lives, helping with everyday or more important issues. With this in mind, I started studying programming with the intention of creating something, something that could help in some way. I'm currently studying at EBAC, where I'm specializing as a JavaScript developer and its freamworks like Vue.js and React.Come check out some of the projects!"/>
      
    </div>
    
    <TextSection 
    title='Courses' 
    text="EBAC - Front-end developer"
    secondText="
  The EBAC Front-End course was a deep dive into web development, covering HTML, CSS, and JavaScript fundamentals. We explored popular frameworks like Vue.js and React.js, learned about agile practices, front-end architecture, and API integration. The course also touched on version control with Git and introduced optimization techniques. Tools like Webpack and Gulp were used for workflow automation. Emphasis on collaborative projects highlighted the significance of teamwork in front-end development."
    />
    <div class="section-button">
        <TheButtons class="button" title='My Projects'/>
    </div>
  </main>
</template>

<style scoped>
  .button {
    margin: 2rem auto;
  }
  .section-button{
    display: flex;
    justify-content: center;
  }
</style>