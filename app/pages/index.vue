<script setup>
definePageMeta({ layout: 'home' })
</script>

<template>
  <Header />
  
  <div class="bg-background min-h-screen">
    <div class="relative w-full h-screen bg-black overflow-hidden flex items-center">
      <img src="/assets/images/banner2.png" alt="Beer" class="absolute right-0 bottom-0 h-[40%] sm:h-[80%] lg:h-[85%] object-cover">

      <div class="relative z-10 flex flex-col justify-center px-6 sm:px-10 lg:px-24 w-full max-w-full lg:max-w-[60%]">
        <h1 class="text-white font-header text-3xl sm:text-4xl lg:text-5xl uppercase tracking-widest">CAMBODIAN CRAFT</h1>
        <h1 class="text-primary font-header text-3xl sm:text-4xl lg:text-5xl uppercase tracking-wider mt-1">BEER CROWN 2026</h1>
        <p class="text-white font-primary text-base sm:text-lg mt-4 leading-relaxed max-w-lg">
          Classic European Beer Style — Inspired by centuries of European brewing excellence, 
          offering a refined taste, golden clarity, and an exceptionally smooth drinking experience.
        </p>
        <NuxtLink to="https://docs.google.com/forms/d/e/1FAIpQLScEjueBWitDWygOZkaHDnkADWIHhYdgZ-lH_u3EvKM2RzL1AA/viewform" target="_blank" class="mt-8 self-start bg-primary text-white px-6 sm:px-8 py-3 font-header text-xs sm:text-sm uppercase tracking-widest hover:bg-accent transition-colors">
          JUDGE HERE
        </NuxtLink>
      </div>
    </div>

    <section class="mx-auto px-6 xl:px-[60px] py-12 sm:py-20">
      <div class="grid grid-cols-1 lg:grid-cols-2 items-center gap-8 sm:gap-[50px]">
        <div class="text-center lg:text-right">
          <h1 class="text-header font-header text-3xl sm:text-4xl lg:text-5xl uppercase tracking-widest">Welcome to <br class="hidden sm:block">CAMBODIAN CRAFT</h1>
          <h1 class="font-header text-3xl sm:text-4xl lg:text-5xl uppercase tracking-wider text-primary mt-2">BEER CROWN 2026</h1>
        </div>
        
        <p class="border-l-10 sm:border-l-10 border-primary bg-card p-6 sm:p-8 font-primary text-context leading-relaxed text-justify rounded-[10px]">
          Welcome to our Beer Tasting & Voting Event! Today, you'll have the opportunity to explore a 
          carefully selected range of beers, each offering its own unique character, aroma, and flavor profile. 
          Take your time to taste, compare, and discover your favorites. Once you've sampled the selection, 
          cast your vote and help us determine the People's Choice Winner. We hope you enjoy the experience 
          and raise a glass to great beer and great company. Cheers!
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-12">
        <div class="bg-card p-6 rounded-[10px] flex flex-col gap-6 border border-gray-200">
          <div class="bg-background px-4 py-3 rounded-[10px] flex items-center justify-between border border-gray-200">
            <Icon name="solar:magnifer-bold-duotone" size="30px" class="text-primary" />
            <h3 class="font-header text-lg tracking-wide text-header">DISCOVER</h3>
          </div>
          <p class="font-primary text-sm sm:text-base leading-relaxed text-context px-1">
            Explore a curated selection of beers and uncover the unique qualities that define each brew, from aroma and flavor to finish and balance.
          </p>
        </div>

        <div class="bg-card p-6 rounded-[10px] flex flex-col gap-6 border border-gray-200">
          <div class="bg-background px-4 py-3 rounded-[10px] flex items-center justify-between border border-gray-200">
            <Icon name="solar:cup-hot-bold-duotone" size="30px" class="text-primary" />
            <h3 class="font-header text-lg tracking-wide text-header">SAVOR</h3>
          </div>
          <p class="font-primary text-sm sm:text-base leading-relaxed text-context px-1">
            Take a moment to appreciate the craftsmanship behind every sip. Notice the subtle notes, texture, and character that make each beer memorable.
          </p>
        </div>

        <div class="bg-card p-6 rounded-[10px] flex flex-col gap-6 border border-gray-200">
          <div class="bg-background px-4 py-3 rounded-[10px] flex items-center justify-between border border-gray-200">
            <Icon name="solar:crown-bold-duotone" size="30px" class="text-primary" />
            <h3 class="font-header text-lg tracking-wide text-header">SELECT</h3>
          </div>
          <p class="font-primary text-sm sm:text-base leading-relaxed text-context px-1">
            Choose the beer that delivered the most enjoyable experience and submit your vote to help crown the event champion.
          </p>
        </div>
      </div>
    </section>

    <Footer />
  </div>
</template>