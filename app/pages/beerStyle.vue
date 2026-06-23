<script setup>
import { ref, computed } from 'vue'

const searchQuery = ref('')

const beerStyles = ref([
  {
    name: 'Strong Bitter (ESB)',
    origin: 'England',
    abv: '4.6% – 6.2%',
    ibu: '30 - 50',
    description: 'An average- to strong-strength English ale featuring a nice balance between leafy, earthy British hops and a solid malt backbone. Expect notes of biscuit, nut, or caramel with a dry, clean finish.'
  },
  {
    name: 'English IPA',
    origin: 'England',
    abv: '5.0% – 7.5%',
    ibu: '40 - 60',
    description: 'A hoppy, moderately strong British pale ale that leans into herbal, floral, and spicy wood qualities rather than the bright citrus of its American cousin. The malt profile is often more prominent here, presenting toasted, bready, or caramel layers.'
  },
  {
    name: 'Witbier',
    origin: 'Belgium',
    abv: '4.5% – 5.5%',
    ibu: '8 - 20',
    description: 'A remarkably refreshing, pale wheat ale brewed with coriander and curaçao orange peel. It is intentionally hazy from unmalted wheat and yeast, offering a bright, citrusy, and subtly spicy flavor profile.'
  },
  {
    name: 'Saison',
    origin: 'Belgium',
    abv: '3.5% – 9.5%',
    ibu: '20 - 35',
    description: 'An artisanal, highly carbonated Belgian farmhouse ale with a distinctive dry, fruity, and peppery character. It balances complex esters and phenols with a prominent hop bitterness and an incredibly candy finish.'
  },
  {
    name: 'Weißbier',
    origin: 'Germany',
    abv: '4.3% – 5.6%',
    ibu: '8 - 15',
    description: 'A traditional South German wheat beer famous for its cloudy appearance and dramatic yeast-driven aromas of banana and clove. It has low bitterness, high carbonation, and a fluffy, creamy mouthfeel.'
  },
  {
    name: 'German Pils',
    origin: 'Germany',
    abv: '4.4% – 5.2%',
    ibu: '22 - 40',
    description: 'A crisp, clean, and highly attenuated gold-colored lager that highlights noble German hops like Hallertau or Tettnanger. It features a distinctive, snappy floral aroma and a firm, lingering bitterness.'
  },
  {
    name: 'Munich Dunkel',
    origin: 'Germany',
    abv: '4.5% – 5.6%',
    ibu: '18 – 28',
    description: 'A classic, deeply comforting dark lager from Bavaria that celebrates rich, bready, and toasty Munich malts. It tastes of bread crusts, nuts, or mild chocolate without ever feeling heavy, overly sweet, or roasted like a stout.'
  }
])

// Computed property to filter styles by name, origin, or description
const filteredBeerStyles = computed(() => {
  return beerStyles.value.filter(style => {
    const query = searchQuery.value.toLowerCase()
    return (
      style.name.toLowerCase().includes(query) ||
      style.origin.toLowerCase().includes(query)
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
            Beer Styles
          </h1>
          <p class="font-primary text-context text-sm">
            Explore traditional global beer profiles, historical origins, and characteristics.
          </p>
        </div>

        <div class="relative w-full md:w-80 target-right">
          <span class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
            <Icon name="solar:magnifer-linear" size="20px" class="text-gray-400" />
          </span>
          <input 
            v-model="searchQuery"
            type="text" 
            placeholder="Search styles, origins..." 
            class="w-full pl-10 pr-4 py-2.5 bg-white border border-gray-200 rounded-xl font-primary text-sm focus:outline-none focus:ring-2 focus:ring-primary/20 focus:border-primary transition-all"
          />
        </div>
      </div>

      <div class="beer-styles-grid">
        <div 
          v-for="(style, index) in filteredBeerStyles"  
          :key="index"
          class="bg-card rounded-xl p-5 flex flex-col justify-between gap-4 border border-gray-100 border border-gray-200"
        >
          <div class="flex flex-col gap-3 text-left w-full">
            <div>
              <h2 class="font-header text-primary text-[22px] uppercase tracking-wide leading-tight">
                {{ style.name }}
              </h2>
              <span class="inline-block bg-background text-gray-700 font-medium text-xs px-2.5 py-1 rounded-full mt-1">
                Origin: {{ style.origin }}
              </span>
            </div>

            <div class="specs-grid text-header font-header text-[12px]">
              <div class="bg-white border border-gray-200 p-[10px] rounded-[10px] flex items-center gap-2">
                <Icon name="solar:wineglass-triangle-bold-duotone" size="25px" class="text-primary" />
                <span><strong>ABV:</strong> {{ style.abv }}</span>
              </div>
              
              <div class="bg-white border border-gray-200 p-[10px] rounded-[10px] flex items-center gap-2">
                <Icon name="solar:bomb-emoji-bold-duotone" size="25px" class="text-primary" />
                <span><strong>IBU:</strong> {{ style.ibu }}</span>
              </div>
            </div>

            <p class="font-primary text-context text-[14px] leading-relaxed mt-2 border-t border-gray-100 pt-3">
              {{ style.description }}
            </p>
          </div>
        </div>
      </div>

      <div v-if="filteredBeerStyles.length === 0" class="text-center py-12">
        <p class="font-primary text-gray-400 text-base">No beer styles match your search.</p>
      </div>

    </main>

    <footer class="bg-primary text-text-accent text-center py-4 text-xs md:text-sm font-primary w-full">
      © Craft Beer Association Guide • Global Beer Styles Reference
    </footer>
  </div>
</template>

<style scoped>
.beer-styles-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
  width: 100%;
}

@media (min-width: 768px) {
  .beer-styles-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1280px) {
  .beer-styles-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

.specs-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}
</style>