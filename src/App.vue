<template>
  <div class="resume-container">
    <Header />
    <Profile />
    <Experience />
    <Education />
    <Skills />
    <Projects />
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
.resume-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}
</style>