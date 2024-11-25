<template>
  <div class="resume-container">
    <nav class="navbar">
      <ul>
        <li><a href="#" @click="showSection('header')">Header</a></li>
        <li><a href="#" @click="showSection('profile')">Profile</a></li>
        <li><a href="#" @click="showSection('experience')">Experience</a></li>
        <li><a href="#" @click="showSection('education')">Education</a></li>
        <li><a href="#" @click="showSection('skills')">Skills</a></li>
        <li><a href="#" @click="showSection('projects')">Projects</a></li>
      </ul>
    </nav>

    <!-- Conditional rendering of sections -->
    <div v-if="currentSection === 'header'" id="header">
      <Header />
    </div>
    <div v-if="currentSection === 'profile'" id="profile">
      <Profile />
    </div>
    <div v-if="currentSection === 'experience'" id="experience">
      <Experience />
    </div>
    <div v-if="currentSection === 'education'" id="education">
      <Education />
    </div>
    <div v-if="currentSection === 'skills'" id="skills">
      <Skills />
    </div>
    <div v-if="currentSection === 'projects'" id="projects">
      <Projects />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Education from './components/Education.vue'
import Experience from './components/Experience.vue'
import Header from './components/Header.vue'
import Profile from './components/Profile.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'

const currentSection = ref('header') // Default section to be shown

function showSection(section: string) {
  currentSection.value = section
}
</script>

<style scoped>
.resume-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.navbar {
  margin-bottom: 20px;
}

.navbar ul {
  list-style-type: none;
  padding: 0;
}

.navbar li {
  display: inline;
  margin-right: 15px;
}

.navbar a {
  text-decoration: none;
  color: black;
}
</style>
