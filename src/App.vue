<script setup lang="ts">
import NavigationBar from "./components/NavigationBar.vue";
import MySkills from "./components/MySkills.vue";
import MyAwards from "./components/MyAwards.vue";
import AboutMe from "./components/AboutMe.vue";
import MyEducation from "./components/MyEducation.vue";
import MyInterests from "./components/MyInterests.vue";
import MyExperience from "./components/MyExperience.vue";
import jsonData from "./myData.json";

const { navItems, interest, accomplishment, education, experience, social, user, skills, responsibility } = jsonData;
</script>

<template>
  <div class="main-wrapper">
    <NavigationBar landing-link="#about" :navItems="navItems" id="sideNav"></NavigationBar>
    <div class="container-fluid p-0">
      <AboutMe :user="user" :social="social" id="about"></AboutMe>
      <MyExperience :experience="experience" id="experience"></MyExperience>
      <MyEducation :education="education" id="education"></MyEducation>
      <MySkills :skills="skills" :responsibility="responsibility" id="skills"></MySkills>
      <MyInterests :interest="interest" id="interests"></MyInterests>
      <MyAwards :accomplishment="accomplishment" id="awards"></MyAwards>
    </div>
  </div>
</template>
