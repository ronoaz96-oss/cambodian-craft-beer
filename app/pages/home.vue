<template>
  <div>
    <TheHeader />

    <!-- Hero Section -->
    <div class="relative w-full h-screen bg-black overflow-hidden pt-14 flex items-center">

      <!-- Beer bottle image (right side) -->
      <img
        src="~/assets/image/beer.png"
        alt="Beer"
        class="absolute right-0 bottom-0 h-[85%]  sm:h-[75%] md:h-[80%] lg:h-[85%] xl:h-[90%] object-contain">

      <!-- Content (left side) -->
      <div class="relative z-10 bottom-40 flex flex-col justify-center h-full px-4 sm:px-6 md:px-10 lg:px-16 xl:px-24 w-full max-w-[75%] sm:max-w-[55%] md:max-w-[50%] lg:max-w-[45%]">
        <h2 class="text-white font-bold text-2xl sm:text-base md:text-lg lg:text-2xl uppercase tracking-wide">
          CAMBODIAN CRAFT
        </h2>

        <h1 class="text-[#800020] font-bold text-2xl sm:text-xl md:text-2xl lg:text-3xl xl:text-4xl uppercase tracking-wide mt-1">
          BEER CROWN 2026
        </h1>

        <p class="text-white text-xl sm:text-sm md:text-base mt-3 md:mt-4 leading-relaxed">
          Classic European Beer Style Inspired by centuries of European brewing excellence,
          offering a refined taste, golden clarity, and an exceptionally smooth drinking experience.
        </p>

        <button class=" mt-5 md:mt-6 self-start bg-[#800020] text-white px-4 sm:px-5 md:px-6 py-2 rounded-full text-xs sm:text-sm font-bold uppercase tracking-widest hover:bg-[#600018 transition-colors">
           JUDGE HERE
        </button>
      </div>
    </div>
\
    <section class="px-4 sm:px-6 md:px-10 lg:px-16 xl:px-24 py-8 sm:py-10 md:py-14 bg-white">


      <h2 class="text-center font-bold text-xl sm:text-lg md:text-xl uppercase">
        Welcome to CAMBODIAN CRAFT
      </h2>
      <h1 class="text-center font-bold text-xl sm:text-2xl md:text-3xl uppercase text-[#800020]">
        BEER CROWN 2026
      </h1>

     
      <p class="bg-[#F2F2F2] border-l-4 mb-5 border-[#800020] font-medium rounded-lg p-3 sm:p-4 mt-5 sm:mt-6 text-[12px] sm:text-sm md:text-base text-gray-700 leading-relaxed text-justify">
        Welcome to our Beer Tasting &amp; Voting Event! Today, you'll have the opportunity to explore a carefully selected range of beers, each offering its own unique character, aroma, and flavor profile. Take your time to taste, compare, and discover your favorites. Once you've sampled the selection, cast your vote and help us determine the People's Choice Winner. We hope you enjoy the experience and raise a glass to great beer and great company. Cheers!
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">

        <!-- Card 1: DISCOVER -->
        <div class="border bg-[#F2F2F2] border-gray-100 rounded-xl p-4 shadow-sm flex flex-col gap-2">
          <div class="flex bg-white p-3 rounded-xl items-center justify-between">
           
            <span class="text-[#800020] text-xl"></span>
            <span class="font-bold tracking-widest uppercase text-sm sm:text-base">DISCOVER</span>
          </div>
          <p class="text-[12px] sm:text-sm font-medium text-gray-600">
            Explore a curated selection of beers and uncover the unique qualities that define each brew, from aroma and flavor to finish and balance.
          </p>
        </div>

        <!-- Card 2: SAVOR -->
        <div class="border bg-[#F2F2F2] border-gray-100 rounded-xl p-4 shadow-sm flex flex-col gap-2">
          <div class="flex bg-white p-3 rounded-xl items-center justify-between">
            
            <span class="text-[#800020] text-xl"></span>
            <span class="font-bold tracking-widest uppercase text-sm sm:text-base">SAVOR</span>
          </div>
          <p class="text-[12px] sm:text-sm font-medium text-gray-600">
            Take a moment to appreciate the craftsmanship behind every sip. Notice the subtle notes, texture, and character that make each beer memorable.
          </p>
        </div>

        <!-- Card 3: SELECT -->
        <div class="border bg-[#F2F2F2] border-gray-100 rounded-xl p-4 shadow-sm flex flex-col gap-2">
          <div class="flex bg-white p-3 rounded-xl items-center justify-between">
       
            <span class="text-[#800020] text-xl"></span>
            <span class="font-bold tracking-widest uppercase text-sm sm:text-base">SELECT</span>
          </div>
          <p class="text-[12px] sm:text-sm font-medium text-gray-600">
            Choose the beer that delivered the most enjoyable experience and submit your vote to help crown the event champion.
          </p>
        </div>

      </div>
    </section>
    <TheFooter />
  </div>
</template>