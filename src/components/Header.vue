<template>
<header id="header" class="sticky top-0 left-0 w-full px-12 py-4 border-b border-gray-600 z-[999] bg-opacity-50 backdrop-blur-3xl">
    <nav class="flex items-center justify-between">
      <!-- Logo -->
      <div class="text-white font-bold text-lg">
        <a href="#" class="logo-link">My Portfolio</a>
      </div>

      <!-- Hamburger Button -->
      <button @click="menuOpen = !menuOpen" class="lg:hidden text-white">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
             viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round"
                d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
      </button>

      <!-- Desktop Menu -->
      <ul class="hidden lg:flex space-x-8 mr-28 text-gray-400">
        <li v-for="(link, index) in navLinks" :key="index">
          <a 
            :href="link.href" 
            @click="smoothScroll"
            class="nav-link"
          >
            {{ link.text }}
          </a>
        </li>
      </ul>
    </nav>

    <!-- Mobile Menu -->
    <transition name="slide">
      <ul
        v-if="menuOpen"
        class="lg:hidden mt-4 bg-white rounded-2xl shadow-xl p-6 text-center space-y-4 text-gray-700 absolute top-16 right-6 w-52 z-50"
      >
        <li v-for="(link, index) in navLinks" :key="index">
          <a 
            :href="link.href" 
            @click="closeMenuAndScroll"
            class="mobile-nav-link"
          >
            {{ link.text }}
          </a>
        </li>
      </ul>
    </transition>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const navLinks = ref([
  { href: '#home', text: 'Home' },
  { href: '#about', text: 'About' },
  { href: '#skills', text: 'Skills' },
  { href: '#projects', text: 'Projects' },
  { href: '#contact', text: 'Contact' }
])

const smoothScroll = (e) => {
  e.preventDefault()
  const targetId = e.target.getAttribute('href')
  const targetElement = document.querySelector(targetId)
  if (targetElement) {
    window.scrollTo({
      top: targetElement.offsetTop - 80, // Adjust for header height
      behavior: 'smooth'
    })
  }
}

const closeMenuAndScroll = (e) => {
  menuOpen.value = false
  smoothScroll(e)
}
</script>

<style scoped>
/* Fade transition for overlay effect */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}

/* Slide transition for mobile menu */
.slide-enter-active {
  animation: slide-down 0.3s ease-out;
}
.slide-leave-active {
  animation: slide-up 0.3s ease-in;
}

@keyframes slide-down {
  from {
    transform: translateY(-20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes slide-up {
  from {
    transform: translateY(0);
    opacity: 1;
  }
  to {
    transform: translateY(-20px);
    opacity: 0;
  }
}

/* Logo hover animation */
.logo-link {
  position: relative;
  display: inline-block;
  transition: color 0.3s ease;
}

.logo-link:hover {
  color: #4ade80; /* Green-500 color */
}

.logo-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: #4ade80;
  transition: width 0.3s ease;
}

.logo-link:hover::after {
  width: 100%;
}

/* Desktop nav link hover animation */
.nav-link {
  position: relative;
  display: inline-block;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: white;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: #4ade80;
  transition: width 0.3s ease, transform 0.3s ease;
  transform: scaleX(0);
  transform-origin: right center;
}

.nav-link:hover::after {
  width: 100%;
  transform: scaleX(1);
  transform-origin: left center;
}

/* Mobile nav link hover animation */
.mobile-nav-link {
  position: relative;
  display: inline-block;
  padding: 8px 0;
  transition: color 0.3s ease;
}

.mobile-nav-link:hover {
  color: #4ade80;
}

.mobile-nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 4px;
  left: 50%;
  background-color: #4ade80;
  transition: width 0.3s ease, left 0.3s ease;
}

.mobile-nav-link:hover::after {
  width: 100%;
  left: 0;
}
</style>