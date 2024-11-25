<template>
  <div class="resume-container">
    <nav class="navbar">
      <ul>
        <li><a href="#header">Header</a></li>
        <li><a href="#profile">Profile</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
      </ul>
    </nav>

    <div id="header">
      <Header />
    </div>
    <div id="profile">
      <Profile />
    </div>
    <div id="experience">
      <Experience />
    </div>
    <div id="education">
      <Education />
    </div>
    <div id="skills">
      <Skills />
    </div>
    <div id="projects">
      <Projects />
    </div>
  </div>
</template>


<script setup lang="ts">
import Education from './components/Education.vue'
import Experience from './components/Experience.vue'
import Header from './components/Header.vue'
import Profile from './components/Profile.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
</script>

<style scoped>
.navbar {
  background-color: #333;
  padding: 10px 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
}
.navbar ul {
  list-style-type: none;
  display: flex;
  justify-content: space-around;
  margin: 0;
  padding: 0;
}
.navbar li {
  margin: 0 10px;
}
.navbar a {
  color: white;
  text-decoration: none;
  font-size: 16px;
}
.navbar a:hover {
  text-decoration: underline;
}
.resume-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}
html {
  scroll-behavior: smooth;
}
</style>
