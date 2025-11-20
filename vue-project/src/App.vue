<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { useRouter } from 'vue-router'
import Projects from './components/Projects.vue';
import AboutMe from './components/AboutMe.vue';
import Publications from './components/Publications.vue';

import Certifications from './components/Certifications.vue';

const router = useRouter();

function aboutme(){
  router.push({name: "AboutMe"});  
}

function projects(){
  console.log("Projects");
  router.push({name: "Projects"});
}

function publications(){
  router.push({name: "Publications"});
}

function certifications(){
  router.push({name: "Certifications"})
}

</script>

<template>
  <div class="navbar">
    <ul class="navbar-list">
      <li>
        <div class="navbar-section" @click="aboutme">
          About Me
        </div>
      </li>
      <li>
        <div class="navbar-section" @click="projects">
          Projects
        </div>
      </li>
      <li>
        <div class="navbar-section" @click="publications">
          Volunteering
        </div>
      </li>
      <li>
        <div class="navbar-section" @click="certifications">
          Certifications
        </div>
      </li>
    </ul>
  </div>

  <RouterView />

</template>

<style scoped>
.navbar {
  width: 100%; /* full width */
  background-color: #fbfaf9;
  padding: 1rem 0;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.navbar-inner {
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.navbar-list {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  padding: 0;
  margin: 0;
}

li {
  list-style: none;
}

.navbar-section {
  font-size: 1rem;
  font-weight: 500;
  color: #1B3C53;
  background-color: #D2C1B6;
  padding: 8px 16px;
  border-radius: 8px;
  transition: all 0.3s ease-in-out;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.08);
}

.navbar-section:hover {
  background-color: #456882;
  color: #fbfaf9;
  cursor: pointer;
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

</style>
