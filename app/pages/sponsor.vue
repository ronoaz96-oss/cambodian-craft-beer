<script setup>
import { ref } from 'vue'

const activeIndex = ref(-1)

const toggleDescription = (id) => {
  activeIndex.value = activeIndex.value === id ? -1 : id
}

// Grouped exactly as displayed in the image layout structure
const leftColumn = ref([
  {
    tier: 'Platinum',
    icon: 'solar:medal-ribbon-star-bold-duotone',
    colorClass: 'text-gray-300',
    items: [
      { id: 1, name: 'BERTIE', logo: '/assets/images/bertie.png', tag: 'Official event partner.', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' }
    ]
  },
  {
    tier: 'Gold',
    icon: 'solar:medal-star-circle-bold-duotone',
    colorClass: 'text-amber-500',
    items: [
      { 
        id: 2, 
        name: 'BOTANICO', 
        logo: '/assets/images/botanico.png', 
        tag: 'Premium beer supplier.',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' 
      },
      { id: 3, name: 'CRAFT BEER ASSOCIATION', logo: '/assets/images/cba.png', tag: 'Local food provider.', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' }
    ]
  }
])

const rightColumn = ref([
  {
    tier: 'Silver',
    icon: 'solar:cup-bold-duotone',
    colorClass: 'text-zinc-400',
    items: [
      { id: 4, name: 'THAI TAN', logo: '/assets/images/thaitan.png', tag: 'Community supporter.', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' },
      { id: 5, name: 'YAKIMA CHIEF', logo: '/assets/images/yakima.png', tag: 'Craft beer enthusiast group.', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' }
    ]
  },
  {
    tier: 'Regular Partners',
    icon: 'solar:users-group-two-rounded-bold-duotone',
    colorClass: 'text-amber-600',
    items: [
      { id: 6, name: 'SKAI TECH', logo: '/assets/images/skaitech.png', tag: 'Event logistics partner.', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placeholder for information.' }
    ]
  }
])
</script>

<template>
  <div class="bg-background min-h-screen flex flex-col justify-between">
    <main class="mx-4 xl:mx-[60px] my-10 flex-grow">
      
      <div class="text-center mb-10">
        <h1 class="font-header text-primary text-4xl uppercase tracking-wider mb-2">
          Sponsors
        </h1>
        <p class="font-primary text-context text-sm max-w-2xl mx-auto">
          We thank our generous sponsors who make the Cambodian Craft Beer Crown 2025 possible.
        </p>
      </div>

      <div class="grid grid-cols-1 xl:grid-cols-2 gap-8 items-start">
        
        <div class="flex flex-col gap-8">
          <div v-for="(group, gIndex) in leftColumn" :key="'left-'+gIndex" class="flex flex-col gap-3">
            <div class="flex items-center gap-2 font-header text-header text-lg uppercase tracking-wide">
              <Icon :name="group.icon" size="24px" :class="group.colorClass" />
              <span>{{ group.tier }}</span>
            </div>
            
            <div class="bg-card rounded-xl p-4 flex flex-col gap-4">
              <div 
                v-for="item in group.items" 
                :key="item.id"
                @click="toggleDescription(item.id)"
                class="bg-white rounded-lg p-6 flex flex-col gap-4 cursor-pointer transition-all duration-200 shadow-xs"
              >
                <div class="flex items-center justify-between w-full">
                  <div class="h-14 w-32 flex items-center justify-start">
                    <img :src="item.logo" :alt="item.name" class="max-h-full max-w-full object-contain">
                  </div>
                  <span class="font-header text-header text-right text-lg xl:text-xl uppercase tracking-wide">
                    {{ item.name }}
                  </span>
                </div>
                
                <div v-if="activeIndex === item.id" class="flex flex-col gap-3 mt-1 border-t border-gray-100 pt-4">
                  <div v-if="item.tag" class="self-start bg-card text-context text-xs p-[10px] rounded font-primary">
                    {{ item.tag }}
                  </div>
                  <p class="text-context text-xs md:text-sm leading-relaxed font-primary">
                    {{ item.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-col gap-8">
          <div v-for="(group, gIndex) in rightColumn" :key="'right-'+gIndex" class="flex flex-col gap-3">
            <div class="flex items-center gap-2 font-header text-header text-lg uppercase tracking-wide">
              <Icon :name="group.icon" size="24px" :class="group.colorClass" />
              <span>{{ group.tier }}</span>
            </div>
            
            <div class="bg-card rounded-xl p-4 flex flex-col gap-4">
              <div 
                v-for="item in group.items" 
                :key="item.id"
                @click="toggleDescription(item.id)"
                class="bg-white rounded-lg p-6 flex flex-col gap-4 cursor-pointer transition-all duration-200 shadow-xs"
              >
                <div class="flex items-center justify-between w-full">
                  <div class="h-14 w-32 flex items-center justify-start">
                    <img :src="item.logo" :alt="item.name" class="max-h-full max-w-full object-contain">
                  </div>
                  <span class="font-header text-header text-right text-lg xl:text-xl uppercase tracking-wide">
                    {{ item.name }}
                  </span>
                </div>

                <div v-if="activeIndex === item.id" class="flex flex-col gap-3 mt-1 border-t border-gray-100 pt-4">
                  <div v-if="item.tag" class="self-start bg-card text-context text-xs p-[10px] rounded font-primary">
                    {{ item.tag }}
                  </div>
                  <p class="text-context text-xs md:text-sm leading-relaxed font-primary">
                    {{ item.description }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </main>

    <footer class="bg-primary text-text-accent text-center py-4 text-xs md:text-sm font-primary mt-12 w-full">
      © CBAC — Cambodian Craft Beer Association • Event: 16 August 2025 • Botanico Craft Beer Garden
    </footer>
  </div>
</template>