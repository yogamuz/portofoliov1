<template>
  <section id="home" class="hero bg-base-200 px-4 md:px-12 py-8">
    <div
      class="flex flex-col md:flex-row items-center justify-center w-full gap-10 max-w-7xl mx-auto"
    >
      <!-- Konten Kiri -->
      <div class="hero-content text-center lg:text-left flex-1">
        <div>
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-2 text-white">
            I am <span class="text-[color:#bd9f67]">Prayogo</span>
          </h1>
          <p class="py-3 text-lg font-medium text-white">Web Developer</p>
          <p class="pb-6 text-white">
            I have keep interest in Web Development, believing that
            presenting an attractive design is crucial for a website. I am
            always eager to learn new things and improve my skills.
          </p>
        </div>
        <div class="mt-4 flex flex-col sm:flex-row justify-center lg:justify-start gap-4">
          <button @click="downloadCv"
            class="px-5 py-2 text-green-500 border border-green-500 rounded-sm hover:bg-green-500 hover:text-white transition"
          >
            Download CV
          </button>
          <button
            class="px-5 py-2 text-white border border-white rounded-sm hover:bg-white hover:text-black transition"
          >
            More
          </button>
        </div>
      </div>

      <!-- Konten Kanan -->
      <div class="hero-image flex flex-col items-center flex-1">
        <div class="relative group">
          <!-- 3D Rounded Image Container -->
          <div class="rounded-full p-1 bg-gradient-to-br from-[#bd9f67] via-[#d4b87c] to-[#a78a56] shadow-xl transform group-hover:rotate-3 transition-transform duration-300">
            <!-- Inner white border -->
            <div class="rounded-full p-1 bg-white">
              <!-- Main image with shadow -->
              <img
                src="../assets/avatar.jpg"
                alt="Hero Image"
                class="rounded-full w-48 h-48 md:w-56 md:h-56 object-cover border-4 border-white shadow-2xl transform group-hover:-rotate-3 transition-transform duration-300"
              />
            </div>
          </div>
          
          <!-- Floating gold circles for 3D effect -->
          <div class="absolute -top-2 -left-2 w-4 h-4 rounded-full bg-[#bd9f67] opacity-70 group-hover:opacity-100 transition-opacity"></div>
          <div class="absolute -bottom-2 -right-2 w-4 h-4 rounded-full bg-[#bd9f67] opacity-70 group-hover:opacity-100 transition-opacity"></div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const downloadCv = () => {
  const fileId = '1Do3rfIuAPEek9edtHbf0_uBA5weep9dk';
  const downloadUrl = `https://drive.google.com/uc?export=download&id=${fileId}`;

  const link = document.createElement('a');
  link.href = downloadUrl;
  link.setAttribute('download', 'cv.pdf'); // nama file saat diunduh
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};
</script>
