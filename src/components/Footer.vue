<template>
  <section id="footer" class="py-24 bg-[#272829]">
    <div class="max-w-5xl mx-auto px-6 text-center">
      <div class="text-white font-bold text-3xl">Yogamuz</div>
      <ul
        class="flex flex-wrap justify-center gap-10 text-white text-sm translate-y-10 mb-8"
      >
        <li v-for="(link, index) in navLinks" :key="index">
          <a
            :href="link.href"
            @click.prevent="smoothScroll(link.href)"
            class="hover:text-green-500 transition-colors duration-300"
          >
            {{ link.text }}
          </a>
        </li>
      </ul>
    </div>

    <div class="flex gap-4 justify-center translate-y-16">
      <ul
        class="example-2 flex flex-wrap justify-center gap-4 sm:gap-6 md:gap-8 lg:gap-10"
      >
        <!-- Social icons remain unchanged -->
        <!-- Telegram -->
        <li class="icon-content">
          <a
            href="https://telegram.org/"
            target="_blank"
            aria-label="Telegram"
            data-social="telegram"
          >
            <div class="filled"></div>
            <svg
              viewBox="0 0 100 100"
              class="w-6 h-6 sm:w-8 sm:h-8 md:w-10 md:h-10"
              fill="currentColor"
            >
              <path
                d="M95,9.9c-1.3-1.1-3.4-1.2-7-0.1c0,0,0,0,0,0c-2.5,0.8-24.7,9.2-44.3,17.3c-17.6,7.3-31.9,13.7-33.6,14.5  c-1.9,0.6-6,2.4-6.2,5.2c-0.1,1.8,1.4,3.4,4.3,4.7c3.1,1.6,16.8,6.2,19.7,7.1c1,3.4,6.9,23.3,7.2,24.5c0.4,1.8,1.6,2.8,2.2,3.2  c0.1,0.1,0.3,0.3,0.5,0.4c0.3,0.2,0.7,0.3,1.2,0.3c0.7,0,1.5-0.3,2.2-0.8c3.7-3,10.1-9.7,11.9-11.6c7.9,6.2,16.5,13.1,17.3,13.9  c0,0,0.1,0.1,0.1,0.1c1.9,1.6,3.9,2.5,5.7,2.5c0.6,0,1.2-0.1,1.8-0.3c2.1-0.7,3.6-2.7,4.1-5.4c0-0.1,0.1-0.5,0.3-1.2  c3.4-14.8,6.1-27.8,8.3-38.7c2.1-10.7,3.8-21.2,4.8-26.8c0.2-1.4,0.4-2.5,0.5-3.2C96.3,13.5,96.5,11.2,95,9.9z M30,58.3l47.7-31.6  c0.1-0.1,0.3-0.2,0.4-0.3c0,0,0,0,0,0c0.1,0,0.1-0.1,0.2-0.1c0.1,0,0.1,0,0.2-0.1c-0.1,0.1-0.2,0.4-0.4,0.6L66,38.1  c-8.4,7.7-19.4,17.8-26.7,24.4c0,0,0,0,0,0.1c0,0-0.1,0.1-0.1,0.1c0,0,0,0.1-0.1,0.1c0,0.1,0,0.1-0.1,0.2c0,0,0,0.1,0,0.1  c0,0,0,0,0,0.1c-0.5,5.6-1.4,15.2-1.8,19.5c0,0,0,0,0-0.1C36.8,81.4,31.2,62.3,30,58.3z"
                fill="currentColor"
              ></path>
            </svg>
          </a>
          <div class="tooltip">Telegram</div>
        </li>

        <!-- Platform X (Twitter) -->
        <li class="icon-content">
          <a href="https://x.com/" 
          target="_blank"
          aria-label="X" 
          data-social="x">
            <div class="filled"></div>
            <svg
              viewBox="0 0 24 24"
              class="w-6 h-6 sm:w-8 sm:h-8 md:w-10 md:h-10"
              fill="currentColor"
            >
              <path
                d="M20.61 3H17.7l-4.31 5.57L9.06 3H3l6.61 9.46L3.34 21h2.91l4.71-6.08L14.94 21H21l-7.05-9.83L20.61 3Z"
              />
            </svg>
          </a>
          <div class="tooltip">X</div>
        </li>

        <!-- Instagram -->
        <li class="icon-content">
          <a
            href="https://instagram.com/"
            target="_blank"
            aria-label="Instagram"
            data-social="instagram"
          >
            <div class="filled"></div>
            <svg
              viewBox="0 0 448 512"
              class="w-6 h-6 sm:w-8 sm:h-8 md:w-10 md:h-10"
              fill="currentColor"
            >
              <path
                d="M224,202.66A53.34,53.34,0,1,0,277.34,256,53.38,53.38,0,0,0,224,202.66Zm124.71-41a54,54,0,0,0-30.6-30.6C293.55,120,224,120,224,120s-69.55,0-94.11,11.06a54,54,0,0,0-30.6,30.6C88,148.45,88,192,88,192s0,43.55,11.06,69.11a54,54,0,0,0,30.6,30.6C154.45,304,224,304,224,304s69.55,0,94.11-11.06a54,54,0,0,0,30.6-30.6C360,235.55,360,192,360,192S360,148.45,348.71,161.66ZM224,272A80,80,0,1,1,304,192,80,80,0,0,1,224,272ZM338.66,153.34a18.66,18.66,0,1,1,18.66-18.66A18.66,18.66,0,0,1,338.66,153.34Z"
              />
            </svg>
          </a>
          <div class="tooltip">Instagram</div>
        </li>

        <!-- LinkedIn -->
        <li class="icon-content">
          <a
            href="https://linkedin.com/"
            target="_blank"
            aria-label="LinkedIn"
            data-social="linkedin"
          >
            <div class="filled"></div>
            <svg
              viewBox="0 0 448 512"
              class="w-6 h-6 sm:w-8 sm:h-8 md:w-10 md:h-10"
              fill="currentColor"
            >
              <path
                d="M100.28 448H7.4V148.9h92.88zM53.79 108.1C24.09 108.1 0 83.74 0 54.14a53.72 53.72 0 0 1 107.44 0c0 29.6-24.09 54-53.65 54zM447.9 448h-92.68V302.4c0-34.7-12.42-58.4-43.45-58.4-23.66 0-37.73 15.93-43.91 31.33-2.26 5.5-2.82 13.1-2.82 20.8V448h-92.68s1.23-267.2 0-294.1h92.68v41.7c12.3-19 34.3-46.1 83.5-46.1 60.9 0 106.6 39.8 106.6 125.3V448z"
              />
            </svg>
          </a>
          <div class="tooltip">LinkedIn</div>
        </li>
      </ul>
    </div>
  </section>
  <div class="px-8 py-4 bg-zinc-950 text-white text-center">
    &copy; 2025 <span class="text-green-500"> Yogamuz </span>. All rights
    reserved. Inc.
  </div>
</template>

<script setup>
import { ref } from "vue";

const navLinks = ref([
  { href: "#home", text: "Home" },
  { href: "#about", text: "About" },
  { href: "#skills", text: "Skills" },
  { href: "#projects", text: "Projects" },
  { href: "#contact", text: "Contact" },
]);

const smoothScroll = (targetId) => {
  const targetElement = document.querySelector(targetId);
  if (targetElement) {
    window.scrollTo({
      top: targetElement.offsetTop - 80, // Adjust for header height
      behavior: "smooth",
    });
  }
};
</script>

<style scoped>
/* Existing social icon styles remain unchanged */
.example-2 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 1px;
  align-items: center;
  transform: translateY(50px);
}

.example-2 .icon-content {
  margin: 0 10px;
  position: relative;
}

.example-2 .icon-content .tooltip {
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  margin-top: 8px;
  color: #fff;
  padding: 6px 10px;
  border-radius: 15px;
  opacity: 0;
  visibility: hidden;
  font-size: 14px;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.example-2 .icon-content:hover .tooltip {
  opacity: 1;
  visibility: visible;
}

.example-2 .icon-content a {
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 24px;
  height: 24px;
  border-radius: 20%;
  color: #4d4d4d;
  background-color: #ffff;
  transition: all 0.3s ease-in-out;
}

.example-2 .icon-content a:hover {
  box-shadow: 3px 2px 45px 0px rgb(0 0 0 / 50%);
}

.example-2 .icon-content a svg {
  position: relative;
  z-index: 1;
  width: 16px;
  height: 16px;
}

.example-2 .icon-content a:hover {
  color: white;
}

.example-2 .icon-content a .filled {
  position: absolute;
  top: auto;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0;
  background-color: #000;
  transition: all 0.3s ease-in-out;
}

.example-2 .icon-content a:hover .filled {
  height: 100%;
}

.example-2 .icon-content a[data-social="telegram"] .filled,
.example-2 .icon-content a[data-social="telegram"] ~ .tooltip {
  background-color: #0088cc;
}

.example-2 .icon-content a[data-social="x"] .filled,
.example-2 .icon-content a[data-social="x"] ~ .tooltip {
  background-color: #000;
}

.example-2 .icon-content a[data-social="instagram"] .filled,
.example-2 .icon-content a[data-social="instagram"] ~ .tooltip {
  background-color: #e1306c;
}

.example-2 .icon-content a[data-social="linkedin"] .filled,
.example-2 .icon-content a[data-social="linkedin"] ~ .tooltip {
  background-color: #0088cc;
}

/* Animation for footer links */
ul.flex-wrap li a {
  position: relative;
  display: inline-block;
}

ul.flex-wrap li a::after {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: #4ade80; /* Green-500 color */
  transition: width 0.3s ease, transform 0.3s ease;
  transform-origin: left center;
}

ul.flex-wrap li a:hover::after {
  width: 100%;
  transform: scaleX(1);
}

/* Slide animation for social icons */
.example-2 {
  animation: slide-up 0.5s ease-out forwards;
}

@keyframes slide-up {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
