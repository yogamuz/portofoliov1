<template>
  <div class="min-h-screen bg-[#2C2C2C]">
    <Header />
    <main>
      <Hero id="home" />
      <About id="about" />
      <Projects id="projects" />
      <Contact id="contact" />
      <Skills id="skills" />
      <Footer />
    </main>
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue"
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
</script>
