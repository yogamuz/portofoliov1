<template>
  <section id="about" class="py-16 bg-[#2C2C2C]">
    <div class="flex flex-col md:flex-row items-center justify-center w-full gap-10 max-w-7xl mx-auto px-4 md:px-12">
      <div class="flex flex-col lg:flex-row items-center gap-8 bg-[#3A3A3A] rounded-xl shadow-2xl overflow-hidden w-full">
        <!-- Image Container - Shows portrait on lg+, landscape on mobile -->
        <div class="w-full lg:w-2/5 relative">
          <!-- Portrait Image (visible on lg+) -->
          <img 
            src="../assets/portrait.jpg" 
            alt="Profile Portrait" 
            class="hidden lg:block w-full h-full min-h-96 object-cover lg:translate-x-6"
          />
          
          <!-- Landscape Image (visible on mobile) -->
          <img 
            src="../assets/landscape.jpeg" 
            alt="Profile Landscape" 
            class="lg:hidden w-full h-64 object-cover"
          />
          
          <!-- Gradient Overlay -->
          <div class="absolute inset-0 bg-gradient-to-b from-[#bd9f67] to-transparent opacity-20 z-10"></div>
          <div class="absolute bottom-0 left-0 right-0 h-16 bg-gradient-to-t from-[#3A3A3A] to-transparent z-10"></div>
        </div>

        <!-- Text Content -->
        <div class="w-full lg:w-3/5 p-8 lg:p-12 text-white">
          <h1 class="text-3xl md:text-4xl font-bold mb-6 text-[#bd9f67]">About Me</h1>
          
          <div class="max-h-64 md:max-h-80 overflow-y-auto pr-4 custom-scroll">
            <p class="text-lg leading-relaxed mb-4">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iure sint
              reprehenderit illo temporibus suscipit dignissimos ea optio vitae
              quisquam, dicta earum! Fuga neque, animi repellat maiores asperiores
              adipisci vero voluptas exercitationem nisi.
            </p>
            <p class="text-lg leading-relaxed mb-4">
              Quasi distinctio, magnam qui voluptas id facere tempore ut sapiente 
              ducimus incidunt doloremque facilis architecto possimus repellat dolorum!
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod.
            </p>
            <p class="text-lg leading-relaxed">
              With over 5 years of experience in frontend development, I specialize in
              creating responsive and user-friendly web applications. My passion lies in
              combining beautiful design with clean, efficient code to deliver exceptional
              digital experiences.
            </p>
          </div>

          <!-- Skills tags -->
          <div class="mt-8 flex flex-wrap gap-3 font-bold">
            <span class="px-3 py-1 bg-[#bd9f67] bg-opacity-20 rounded-full text-sm">HTML/CSS</span>
            <span class="px-3 py-1 bg-[#bd9f67] bg-opacity-20 rounded-full text-sm">JavaScript</span>
            <span class="px-3 py-1 bg-[#bd9f67] bg-opacity-20 rounded-full text-sm">Vue.js</span>
            <span class="px-3 py-1 bg-[#bd9f67] bg-opacity-20 rounded-full text-sm">Tailwind CSS</span>
            <span class="px-3 py-1 bg-[#bd9f67] bg-opacity-20 rounded-full text-sm">Laravel</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Custom scrollbar styling */
.custom-scroll {
  scrollbar-width: thin;
  scrollbar-color: #bd9f67 #3A3A3A;
}

.custom-scroll::-webkit-scrollbar {
  width: 6px;
}

.custom-scroll::-webkit-scrollbar-track {
  background: #3A3A3A;
  border-radius: 3px;
}

.custom-scroll::-webkit-scrollbar-thumb {
  background-color: #bd9f67;
  border-radius: 3px;
}

/* Responsive image adjustments */
@media (max-width: 1023px) {
  .min-h-96 {
    min-height: 24rem; /* 384px */
  }
}
</style>