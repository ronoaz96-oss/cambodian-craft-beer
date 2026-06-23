<script setup>
import { ref, computed } from 'vue'

const searchQuery = ref('')

const breweries = ref([
  {
    logo: '/assets/images/sakpub.png',
    name: 'Sak Pub',
    since: 'SINCE 2021',
    description: 'SAK PUB Craft Beer & Bites opened its taproom and kitchen in October 2021, serving handcrafted in small batch craft beer from taps and giving people a place to savor delicious craft beers in an enjoyable and welcoming atmosphere.',
    facebookUrl: 'https://www.facebook.com/SakPubCraftBeerBites',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/projekt.png',
    name: 'Projekt Brew Co.',
    since: 'SINCE 2020',
    description: 'Projekt brews is a small microbrewery based in Kampot since 2020 making modern hoppy beers.',
    facebookUrl: 'https://www.facebook.com/profile.php?id=100063463360069',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/botanico.png',
    name: 'Botanico Brewing Company',
    since: 'ESTABLISHED',
    description: 'Located in the heart of Phnom Penh, Botanico is one of the oldest craft breweries in the country, creating a big range of different beers, often using locally grown ingredients. The moto is: Real Cambodian Craft Beer!',
    facebookUrl: 'https://www.facebook.com/botanicobrewingco',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/riel.png',
    name: 'Riel Brewing and Distilling',
    since: 'ESTABLISHED',
    description: 'Riel Brewing is a pioneering craft brewery located right here in Phnom Penh, celebrated for helping to establish the local craft beer scene. They are known for their creative and high-quality beers that often incorporate unique Cambodian ingredients.',
    facebookUrl: 'https://www.facebook.com/rielbrewing',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/fuzzylogic.png',
    name: 'Fuzzy Logic',
    since: 'SINCE 2014',
    description: 'Established in 2014, Fuzzy Logic Brewing Co. is one of the pioneers in introducing craft beer to Cambodia and South East Asia. Our brewery has earned a reputation for dedicating itself to consistent, balanced beers. Well known for its Thunderslap IPA and John Lemon Hard Lemonade, Fuzzy Logic has a range of excellent quality products in kegs, cans and bottles and is distributed widely across Cambodia.',
    facebookUrl: 'https://www.facebook.com/FuzzyLogicCambodia',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/chuglab.png',
    name: 'Chug Lab',
    since: 'ESTABLISHED',
    description: 'Chug Brew is a very small nano brewery located in Phnom Penh with the focus on high quality modern craft beers. We also have a heavy metal themed Tap House "Chug Lab" in Bkk3.',
    facebookUrl: 'https://www.facebook.com/thechuglab',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/brewkhnear.png',
    name: 'Brew Khnear',
    since: 'ESTABLISHED',
    description: 'At Brew Khnear, (loosely translated as ‘Brew Together,’) our focus is on getting that work/life balance right. With solid and creative beers made from the finest ingredients using traditional brewing techniques, we strive not to work too hard, but to make time for ourselves and those who are important to us. What better way to bring us all together than drinking good beer.',
    facebookUrl: '',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/funghiart.png',
    name: 'Funghi Art',
    since: 'ESTABLISHED',
    description: 'Create new value for Cambodian rice through fermentation technology. We produce 3 kinds of beer, craft sake, sweet potato and rice Shochu and Gin. All made from Cambodian Rice.',
    facebookUrl: 'https://www.facebook.com/profile.php?id=100069892638809',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/jayavara.png',
    name: 'Jaya-Vara Meadery',
    since: '3 YEARS AGO',
    description: 'Jaya-Vara Meadery has been crafting unique meads and beers in Cambodia for the past 3 years. started as a passion for traditional honey wine has evolved into a full-fledged brewery experimenting with bold flavors and local ingredients.',
    facebookUrl: 'https://www.facebook.com/profile.php?id=100080223013722',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/krama.png',
    name: 'Krama Craft Brewery',
    since: 'ESTABLISHED',
    description: 'Krama Craft Brewery is a cozy craft brewery located in Siem Reap, founded by two partners — one French, one Cambodian. Just minutes from the city center, it offers creative, locally inspired beers like the Triple Khmer and Black IPA. With a warm atmosphere, Cambodian ingredients, and genuine hospitality, Krama is the perfect stop for a unique and authentic craft beer experience in Siem Reap',
    facebookUrl: 'https://www.facebook.com/profile.php?id=100095224728868',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/himawari.png',
    name: 'Himawari Microbrewery',
    since: '1ST HOTEL BREWERY',
    description: 'Himawari Microbrewery is the 1st and only microbrewery launched by it\'s 5-star hotel-apartments in Cambodia. Made from the finest malt and hops, the beers crafted here are unique in flavour and of the highest quality. Himawari Microbrewery\'s brewmaster, Neo, has had many years of brewing experience and has designed 7 exclusive brews, 3 of which have won international awards. There’s definitely a craft beer for every palate.',
    facebookUrl: 'https://www.facebook.com/HimawariHotelMicrobrewery',
    mapUrl: '#'
  },
  {
    logo: '/assets/images/bash.png',
    name: 'Bash Brewing',
    since: 'ESTABLISHED',
    description: 'Bash Brewing is one of the Kingdom’s original craft breweries, creating some of the finest all-natural craft beer in Cambodia.',
    facebookUrl: 'https://www.facebook.com/bashbrewingkh',
    mapUrl: '#'
  }
])

const filteredBreweries = computed(() => {
  return breweries.value.filter(pub => {
    const query = searchQuery.value.toLowerCase()
    return (
      pub.name.toLowerCase().includes(query) ||
      pub.description.toLowerCase().includes(query)
    )
  })
})
</script>

<template>
  <div class="bg-background min-h-screen flex flex-col justify-between">
    <main class="mx-auto w-full my-10 flex-grow px-4 lg:px-[60px]">
      
      <div class="flex flex-col md:flex-row md:items-end md:justify-between gap-6 mb-10 border-b border-gray-100 pb-6">
        <div class="text-left max-w-2xl">
          <h1 class="font-header text-primary text-4xl uppercase tracking-wider mb-2">
            Breweries
          </h1>
          <p class="font-primary text-context text-sm">
            Discover the best craft breweries in Cambodia.
          </p>
        </div>

        <div class="relative w-full md:w-80">
          <span class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
            <Icon name="solar:magnifer-linear" size="20px" class="text-gray-400" />
          </span>
          <input 
            v-model="searchQuery"
            type="text" 
            placeholder="Search breweries..." 
            class="w-full pl-10 pr-4 py-2.5 bg-white border border-gray-200 rounded-xl font-primary text-sm focus:outline-none focus:ring-2 focus:ring-primary/20 focus:border-primary transition-all"
          />
        </div>
      </div>

      <div class="breweries-grid">
        <div 
          v-for="(pub, index) in filteredBreweries"  
          :key="index"
          class="bg-card rounded-xl overflow-hidden flex flex-col justify-between border border-gray-200"
        >
          <div class="w-full h-48 bg-neutral-50 flex items-center justify-center p-6 border-b border-gray-100">
            <img :src="pub.logo" :alt="pub.name" class="max-h-full max-w-[70%] object-contain mix-blend-multiply" />
          </div>

          <div class="p-5 flex flex-col flex-grow gap-2.5 text-left">
            <div>
              <h2 class="font-header text-primary text-[20px] uppercase tracking-wide leading-tight">
                {{ pub.name }}
              </h2>
              
              <div class="inline-flex items-center gap-1.5 bg-background text-gray-700 font-header text-[10px] p-[10px] rounded-md mt-1">
                <Icon name="solar:calendar-minimalistic-bold-duotone" size="14px" class="text-primary" />
                <span>{{ pub.since }}</span>
              </div>
            </div>

            <p class="font-primary text-context text-[14px] leading-relaxed mt-1 flex-grow">
              {{ pub.description }}
            </p>
          </div>

          <div class="p-5 pt-0">
            <div class="buttons-grid font-header text-[11px] tracking-wide">
              <a 
                v-if="pub.facebookUrl"
                :href="pub.facebookUrl" 
                target="_blank" 
                class="bg-white hover:bg-neutral-50 border border-gray-200 text-header rounded-lg p-[8px] flex items-center justify-center gap-1.5 transition-colors"
              >
                <Icon name="solar:link-circle-bold-duotone" size="20px" class="text-primary" />
                <span>Facebook</span>
              </a>
              <div 
                v-else 
                class="bg-gray-50 border border-gray-100 text-gray-400 rounded-lg p-[8px] flex items-center justify-center gap-1.5 cursor-not-allowed"
              >
                <Icon name="solar:link-circle-bold-duotone" size="20px" class="text-gray-300" />
                <span>No Facebook</span>
              </div>
              
              <a 
                :href="pub.mapUrl" 
                target="_blank" 
                class="bg-white hover:bg-neutral-50 border border-gray-200 text-header rounded-lg p-[8px] flex items-center justify-center gap-1.5 transition-colors"
              >
                <Icon name="solar:map-point-bold-duotone" size="20px" class="text-primary" />
                <span>Map</span>
              </a>
            </div>
          </div>

        </div>
      </div>

      <div v-if="filteredBreweries.length === 0" class="text-center py-12">
        <p class="font-primary text-gray-400 text-base">No breweries match your search criteria.</p>
      </div>

    </main>

    <footer class="bg-primary text-text-accent text-center py-4 text-xs md:text-sm font-primary w-full">
      © CBAC — Cambodian Craft Beer Association • Event: 16 August 2025 • Botanico Craft Beer Garden
    </footer>
  </div>
</template>

<style scoped>
.breweries-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
  width: 100%;
}

@media (min-width: 768px) {
  .breweries-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1280px) {
  .breweries-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

.buttons-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
}
</style>