<template>
  <section id="skills" class="py-16 bg-base-100">
    <div class="max-w-5xl mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold text-white mb-12">Tools & Skills</h2>

      <!-- Container untuk sliding animation -->
      <div class="relative overflow-hidden rounded-lg py-4">
        <!-- Gradient overlay untuk fade effect -->
        <div
          class="absolute left-0 top-0 w-32 h-full bg-gradient-to-r from-base-100 to-transparent z-10"
        ></div>
        <div
          class="absolute right-0 top-0 w-32 h-full bg-gradient-to-l from-base-100 to-transparent z-10"
        ></div>

        <!-- Sliding container -->
        <div
          ref="slider"
          class="flex"
          :style="{ transform: `translateX(${translateX}px)` }"
        >
          <!-- Triple set untuk seamless loop -->
          <div v-for="set in 3" :key="set" class="flex">
            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-green-500/20 border-2 border-green-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/vue.svg"
                  alt="Vue.js"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-green-400 transition-colors duration-300"
              >
                Vue JS
              </p>
            </div>

            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-gray-500/20 border-2 border-gray-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/expressjs.svg"
                  alt="Express"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-gray-400 transition-colors duration-300"
              >
                Express JS
              </p>
            </div>
            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-purple-500/20 border-2 border-purple-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/vitejs.svg"
                  alt="Vite"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-purple-400 transition-colors duration-300"
              >
                Vite
              </p>
            </div>

            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-lime-500/20 border-2 border-lime-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/nodejs.png"
                  alt="Node.js"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-lime-400 transition-colors duration-300"
              >
                Node JS
              </p>
            </div>

            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-cyan-500/20 border-2 border-cyan-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/tailwindcss.svg"
                  alt="Tailwind CSS"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-cyan-400 transition-colors duration-300"
              >
                Tailwind
              </p>
            </div>

            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-red-500/20 border-2 border-red-500/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/laravel.svg"
                  alt="Laravel"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-red-400 transition-colors duration-300"
              >
                Laravel
              </p>
            </div>

            <div
              class="flex-shrink-0 mx-4 sm:mx-6 md:mx-8 group cursor-pointer"
            >
              <div
                class="w-16 h-16 sm:w-20 sm:h-20 rounded-xl bg-gray-700/20 border-2 border-gray-600/40 flex items-center justify-center transition-all duration-300 transform group-hover:scale-105 group-hover:shadow-xl"
              >
                <img
                  src="../assets/github.png"
                  alt="GitHub"
                  class="w-8 h-8 sm:w-10 sm:h-10 md:w-12 md:h-12 transition-all duration-300 group-hover:scale-105"
                />
              </div>
              <p
                class="text-white text-sm mt-3 group-hover:text-gray-300 transition-colors duration-300"
              >
                GitHub
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SlidingSkills",
  data() {
    return {
      translateX: 0,
      itemWidth: 0,
      totalItems: 7, // Ubah jadi 7 karena ada tambahan GitHub
      animationId: null,
      speed: 0.4,
      isHovered: false,
    };
  },
  mounted() {
    this.calculateItemWidth();
    this.startAnimation();
    window.addEventListener("resize", this.calculateItemWidth);
  },
  beforeUnmount() {
    this.stopAnimation();
    window.removeEventListener("resize", this.calculateItemWidth);
  },
  methods: {
    calculateItemWidth() {
      this.$nextTick(() => {
        const screenWidth = window.innerWidth;
        if (screenWidth < 640) {
          this.itemWidth = 64 + 32;
        } else if (screenWidth < 768) {
          this.itemWidth = 80 + 48;
        } else {
          this.itemWidth = 80 + 64;
        }
      });
    },
    startAnimation() {
      const animate = () => {
        if (!this.isHovered) {
          this.translateX -= this.speed;

          const oneSetWidth = this.itemWidth * this.totalItems;
          if (Math.abs(this.translateX) >= oneSetWidth) {
            this.translateX = 0;
          }
        }

        this.animationId = requestAnimationFrame(animate);
      };

      this.animationId = requestAnimationFrame(animate);
    },

    stopAnimation() {
      if (this.animationId) {
        cancelAnimationFrame(this.animationId);
      }
    },

    pauseAnimation() {
      this.isHovered = true;
    },

    resumeAnimation() {
      this.isHovered = false;
    },
  },
};
</script>

<style scoped>
.group {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.group:hover ~ * {
  animation-play-state: paused;
}

.flex {
  will-change: transform;
}
</style>
