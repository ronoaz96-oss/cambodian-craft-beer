<template>
  <div class="font-header bg-neutral-50 min-h-screen">
    <main class="w-full mx-auto px-4 lg:px-[60px] py-8 md:py-12">
      
      <div class="text-center mb-8 md:mb-10">
        <h1 class="text-primary text-2xl sm:text-3xl md:text-4xl uppercase tracking-wide mb-2">
          Competition Awards
        </h1>
        <p class="text-context font-primary text-sm sm:text-base">
          Three prestigious categories await our winners
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
        
        <section class="bg-card border border-gray-200 rounded-2xl p-5 md:p-6 flex flex-col justify-between">
          <div>
            <div class="flex items-center justify-between bg-white border border-gray-200 rounded-[10px] px-4 py-2.5 mb-4">
              <span class="text-primary flex items-center">
                <Icon name="solar:users-group-two-rounded-bold-duotone" size="25px" />
              </span>
              <h2 class="text-[16px] font-bold text-header uppercase tracking-wider">
                People's Choice
              </h2>
            </div>

            <span class="inline-block font-primary bg-background text-xs sm:text-sm font-medium text-gray-700 px-3 py-1 rounded-full mb-4">
              Voted by all guests
            </span>

            <p class="font-primary text-[14px] leading-relaxed text-context">
              This is the award judged by you – all our guests.
              To judge, please use the judging form on this website
              and submit one judging per beer.
            </p>
          </div>
        </section>

        <section class="bg-card border border-gray-200 rounded-2xl p-5 md:p-6 flex flex-col justify-between">
          <div>
            <div class="flex items-center justify-between bg-white border border-gray-200 rounded-[10px] px-4 py-2.5 mb-4">
              <span class="text-primary flex items-center">
                <Icon name="solar:crown-line-bold-duotone" size="28px" />
              </span>
              <h2 class="text-[16px] font-bold text-header uppercase tracking-wider">
                Main Award
              </h2>
            </div>

            <span class="inline-block font-primary bg-background text-xs sm:text-sm font-medium text-gray-700 px-3 py-1 rounded-full mb-4">
              Gold, Silver & Bronze
            </span>

            <p class="font-primary text-[14px] leading-relaxed text-context">
              This award is judged by a group of six international experts,
              according to the BJCP score sheet in a blind tasting mode.
              Some of the judges are BJCP certified.
            </p>
          </div>

          <div class="flex flex-wrap gap-2 mt-5 pt-3 border-t border-gray-100">
            <span class="flex items-center gap-1.5 bg-white border border-gray-200 px-3 py-1.5 rounded-[10px] text-xs sm:text-sm font-semibold text-gray-800">
              <Icon name="solar:medal-ribbons-star-bold" size="18px" class="text-amber-400" />
              Gold
            </span>

            <span class="flex items-center gap-1.5 bg-white border border-gray-200 px-3 py-1.5 rounded-[10px] text-xs sm:text-sm font-semibold text-gray-800">
              <Icon name="solar:medal-ribbons-star-bold" size="18px" class="text-gray-400" />
              Silver
            </span>

            <span class="flex items-center gap-1.5 bg-white border border-gray-200 px-3 py-1.5 rounded-[10px] text-xs sm:text-sm font-semibold text-gray-800">
              <Icon name="solar:medal-ribbons-star-bold" size="18px" class="text-amber-700" />
              Bronze
            </span>
          </div>
        </section>

        <section class="bg-card border border-gray-200 rounded-2xl p-5 md:p-6 flex flex-col justify-between">
          <div>
            <div class="flex items-center justify-between bg-white border border-gray-200 rounded-[10px] px-4 py-2.5 mb-4">
              <span class="text-primary flex items-center">
                <Icon name="solar:cup-hot-bold-duotone" size="28px" />
              </span>
              <h2 class="text-[16px] font-bold text-header uppercase tracking-wider">
                Brewer's Choice
              </h2>
            </div>

            <span class="inline-block font-primary bg-background text-xs sm:text-sm font-medium text-gray-700 px-3 py-1 rounded-full mb-4">
              Voted by participating brewers
            </span>

            <p class="font-primary text-[14px] leading-relaxed text-context">
              All brewers participating are also present at the event.
              The brewers judge their fellow competitors' creations.
            </p>
          </div>
        </section>

      </div>
    </main>
  </div>
  <footer class="bg-primary text-text-accent text-center py-4 text-xs md:text-sm font-primary w-full">
    © Craft Beer Association Guide • Global Beer Styles Reference
  </footer>
</template>