<template>
  <section id="contact" class="py-16 bg-base-100 text-white">
    <div
      class="max-w-5xl mx-auto px-6 bg-[#272829] rounded-xl p-6 sm:p-8 flex flex-col gap-6 md:flex-row md:items-center md:justify-between"
    >
      <!-- Caption kiri -->
      <div class="text-center md:text-left">
        <p class="text-xl font-semibold">Have any project in mind?</p>
        <p class="text-sm text-[#a0a0a0]">I'm available for freelancing</p>
      </div>

      <!-- Tombol kanan -->
      <div
        class="flex flex-col sm:flex-row gap-3 sm:gap-4 items-center justify-center md:justify-end"
      >
        <!-- Tombol More Projects -->
        <button
          class="w-full sm:w-auto border border-white text-white px-4 py-2 rounded-md hover:bg-white hover:text-black transition duration-300"
        >
          More Projects
        </button>

        <!-- Tombol Email Me -->
        <button
          @click="openGmailCompose"
          class="w-full sm:w-auto flex items-center justify-center gap-2 border border-green-500 text-green-500 px-4 py-2 rounded-md hover:bg-green-500 hover:text-white transition duration-300"
        >
          <svg
            class="w-4 h-4"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
            />
          </svg>
          Email Me
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const openGmailCompose = () => {
  const email = 'yogagtijr@gmail.com';
  const subject = 'Project Inquiry';
  const body = 'Hello Yogamuz,\n\nI would like to discuss about...\n\nBest regards,';
  
  // URL khusus untuk compose email di Gmail
  const gmailUrl = `https://mail.google.com/mail/?view=cm&fs=1&to=${email}&su=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
  
  // Buka di tab baru
  window.open(gmailUrl, '_blank', 'noopener,noreferrer');
};
</script>