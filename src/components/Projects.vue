<template>
  <section id="projects" class="py-16">
    <div class="max-w-5xl mx-auto px-6 text-center text-white">
      <h1 class="text-3xl font-bold mb-4">Featured Project</h1>
      <p class="text-base leading-relaxed">
        A collection of my featured projects that represent my growth as a web
        developer. Each project demonstrates my focus on clean design,
        functionality, and improving the overall user experience.
      </p>
    </div>

    <div class="my-8 flex justify-center">
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8 justify-items-center mt-10"
      >
        <!-- Card Container -->
        <div
          class="flex flex-col items-center"
          v-for="project in projects"
          :key="project.id"
        >
          <div class="card">
            <div class="content">
              <div class="logo">
                <div class="logo1">
                  <!-- Kosongin kalau nggak perlu logo -->
                </div>
                <div class="logo2"></div>
                <span class="trail"></span>
              </div>

              <!-- Gambar utama project -->
              <div class="logo-bottom-text">
                <div class="image-container">
                  <a :href="project.link" target="_blank">
                    <img :src="project.image" :alt="project.title" />
                  </a>
                </div>
              </div>
            </div>

            <!-- Caption -->
            <span class="bottom-text"> Made by {{ project.author }}</span>
          </div>

          <!-- Project Info - Sekarang di bawah card -->
          <div class="project-info">
            <h3 class="project-title">{{ project.title }}</h3>
            <p class="project-description">
              {{ project.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import projectsData from "../data/projects.json";

const projects = ref(projectsData);
</script>

<style scoped>
/* From Uiverse.io by Smit-Prajapati - Modified */
.card {
  width: 260px;
  height: 300px; /* Dikurangi dari 380px agar tidak lonjong */
  position: relative;
  display: grid;
  margin-bottom: 5px;
  place-content: center;
  border-radius: 10px;
  overflow: hidden;
  transition: all 0.5s ease-in-out;
}

#logo-main,
#logo-second {
  height: 100%;
}

#logo-main {
  fill: #bd9f67;
}

#logo-second {
  padding-bottom: 10px;
  fill: none;
  stroke: #bd9f67;
  stroke-width: 1px;
}

.border {
  position: absolute;
  inset: 0px;
  border: 2px solid #bd9f67;
  opacity: 0;
  transform: rotate(10deg);
  transition: all 0.5s ease-in-out;
}

.bottom-text {
  position: absolute;
  left: 50%;
  bottom: 13px;
  transform: translateX(-50%);
  font-size: 6px;
  text-transform: uppercase;
  padding: 0px 5px 0px 8px;
  color: #bd9f67;
  background: #243137;
  opacity: 0;
  letter-spacing: 7px;
  transition: all 0.5s ease-in-out;
}

.content {
  transition: all 0.5s ease-in-out;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.content .logo {
  height: 35px;
  position: relative;
  width: 33px;
  overflow: hidden;
  transition: all 1s ease-in-out;
}

.content .logo .logo1 {
  height: 33px;
  position: absolute;
  left: 0;
}

.content .logo .logo2 {
  height: 33px;
  position: absolute;
  left: 33px;
}

.content .logo .trail {
  position: absolute;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
}

.content .logo-bottom-text {
  position: relative;
  width: 100%;
  height: 100%;
  transform: none;
  margin-top: 0px;
  padding: 0;
  opacity: 1;
  transition: none;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Styling untuk image container */
.image-container {
  width: 200px; /* Lebar image lebih kecil dari card */
  height: 200px; /* Tinggi image proporsional */
  border-radius: 8px;
  overflow: hidden;
  border: 2px solid #bd9f67;
  opacity: 0.8;
  transition: all 0.3s ease;
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card:hover {
  border-radius: 0;
  transform: scale(1.05); /* Dikurangi dari 1.1 agar tidak terlalu besar */
}

.card:hover .logo {
  width: 134px;
  animation: opacity 1s ease-in-out;
}

.card:hover .border {
  inset: 15px;
  opacity: 1;
  transform: rotate(0);
}

.card:hover .bottom-text {
  letter-spacing: 3px;
  opacity: 1;
  transform: translateX(-50%);
}

.card:hover .content .logo-bottom-text {
  opacity: 1;
  letter-spacing: 9.5px;
}

.card:hover .trail {
  animation: trail 1s ease-in-out;
}

.card:hover .image-container {
  opacity: 1;
  transform: scale(1.02);
}

/* Styling untuk project info di bawah card */
.project-info {
  margin-top: 20px;
  text-align: center;
  color: #bd9f67;
  max-width: 260px;
}

.project-title {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 8px;
  color: #bd9f67;
}

.project-description {
  font-size: 14px;
  line-height: 1.5;
  /* color: #a0a0a0; */
  color: white;
  font: bold;
  margin: 0 auto;
}
</style>
