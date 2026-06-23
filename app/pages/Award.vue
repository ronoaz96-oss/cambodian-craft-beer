<template>
  <div class="font-poppins bg-neutral-50 min-h-screen">
    <main
      class="w-full max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 md:py-12"
    >
      <!-- Title -->
      <div class="text-center mb-8 md:mb-10">
        <h1
          class="text-maroon text-2xl sm:text-3xl md:text-4xl font-extrabold uppercase tracking-wide mb-2"
        >
          Competition Awards
        </h1>

        <p class="text-black text-sm sm:text-base">
          Three prestigious categories await our winners
        </p>
      </div>

      <!-- Awards Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-5">
           <!-- People's Choice Award -->
        <section class="bg-card rounded-2xl p-5 md:p-6">
          <div
            class="flex items-center bg-white rounded-full px-4 py-3 mb-4"
          >
            <span class="text-maroon shrink-0">
              <i class="fa-solid fa-users text-xl sm:text-2xl"></i>
            </span>

            <h2
              class="flex-1 text-right pl-4 text-[14px] sm:text-[10px] md:text-[16px] font-bold text-neutral-900"
            >
              People's Choice Award
            </h2>
          </div>

          <span
            class="inline-block bg-white text-xs sm:text-sm font-medium text-neutral-800 px-4 py-2 rounded-full mb-4"
          >
            Voted by all guests
          </span>

          <p
            class="text-[13px] sm:text-[14px] leading-relaxed text-black"
          >
            This is the award judged by you – all our guests.
            To judge, please use the judging form on this website
            and submit one judging per beer.
          </p>
        </section>

        <!-- Main Award -->
        <section class="bg-card rounded-2xl p-5 md:p-6">
          <div
            class="flex items-center bg-white rounded-full px-4 py-3 mb-4"
          >
            <span class="text-maroon shrink-0">
              <i class="fa-solid fa-crown text-xl sm:text-2xl"></i>
            </span>

            <h2
              class="flex-1 text-right pl-4 text-[14px] sm:text-[10px] md:text-[16px] font-bold text-neutral-900"
            >
              Main Award
            </h2>
          </div>

          <span
            class="inline-block bg-white text-xs sm:text-sm font-medium text-neutral-800 px-4 py-2 rounded-full mb-4"
          >
            Gold, Silver & Bronze
          </span>

          <p
            class="text-[13px] sm:text-[14px] leading-relaxed text-black"
          >
            This award is judged by a group of six international experts,
            according to the BJCP score sheet in a blind tasting mode.
            Some of the judges are BJCP certified.
          </p>

          <div class="flex flex-wrap gap-2 mt-4">
            <span
              class="flex items-center gap-1.5 bg-white px-3 py-2 rounded-full text-xs sm:text-sm font-semibold text-neutral-800"
            >
              <i class="fa-solid fa-medal text-yellow-400"></i>
              Gold
            </span>

            <span
              class="flex items-center gap-1.5 bg-white px-3 py-2 rounded-full text-xs sm:text-sm font-semibold text-neutral-800"
            >
              <i class="fa-solid fa-medal text-gray-400"></i>
              Silver
            </span>

            <span
              class="flex items-center gap-1.5 bg-white px-3 py-2 rounded-full text-xs sm:text-sm font-semibold text-neutral-800"
            >
              <i class="fa-solid fa-medal text-amber-700"></i>
              Bronze
            </span>
          </div>
        </section>

     

        <!-- Brewer's Choice Award -->
        <section class="bg-card rounded-2xl p-5 md:p-6">
          <div
            class="flex items-center bg-white rounded-full px-4 py-3 mb-4"
          >
            <span class="text-maroon shrink-0">
              <i class="fa-solid fa-box-open text-xl sm:text-2xl"></i>
            </span>

            <h2
              class="flex-1 text-right pl-4 text-[14px] sm:text-[10px] md:text-[16px] font-bold text-neutral-900"
            >
              Brewer's Choice Award
            </h2>
          </div>

          <span
            class="inline-block bg-white text-xs sm:text-sm font-medium text-neutral-800 px-4 py-2 rounded-full mb-4"
          >
            Voted by participating brewers
          </span>

          <p
            class="text-[13px] sm:text-[14px] leading-relaxed text-black"
          >
            All brewers participating are also present at the event.
            The brewers judge their fellow competitors' creations.
          </p>
        </section>

      </div>
    </main>
  </div>
</template>

<script setup>
useHead({
  title: 'Competition Awards',
  link: [
    {
      rel: 'stylesheet',
      href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css'
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.gstatic.com',
      crossorigin: ''
    },
    {
      rel: 'stylesheet',
      href:
        'https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap'
    }
  ]
})
</script>
