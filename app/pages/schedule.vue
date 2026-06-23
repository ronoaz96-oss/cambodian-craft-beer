<script setup>
import { ref } from 'vue'

// Track which item index is open (-1 means all closed)
const activeIndex = ref(-1)

const toggleDescription = (index) => {
  if (activeIndex.value === index) {
    activeIndex.value = -1 // Close if clicked again
  } else {
    activeIndex.value = index // Open clicked item
  }
}

const scheduleEvents = ref([
  {
    time: '2:00PM',
    title: 'Event Begin',
    icon: 'solar:clock-circle-bold-duotone',
    description: ''
  },
  {
    time: '3:15PM',
    title: 'Introduction by the MC',
    icon: 'solar:user-speak-bold-duotone',
    description: "An MC introduction sets the stage for the entire event, serving as the bridge between the audience and the upcoming program. A great introduction hooks the crowd's attention immediately, establishes an energetic or appropriate tone, and briefly outlines what guests can look forward to. By blending warmth, clarity, and a touch of charisma, the MC welcomes everyone, introduces themselves, and seamlessly transitions into the main agenda, ensuring the audience feels engaged and excited for what is to come."
  },
  {
    time: '3:30PM',
    title: 'DJ Wha-Wah',
    icon: 'solar:music-notes-bold-duotone',
    description: 'Enjoy custom beats and transitions to keep the energy high.'
  },
  {
    time: '6:40PM',
    title: 'Blind tasting live session',
    icon: 'solar:cup-hot-bold-duotone',
    description: 'Test your tastebuds and guess the craft beers blindly.'
  },
  {
    time: '7:30PM',
    title: 'Start award ceremony',
    icon: 'solar:medal-ribbons-star-bold-duotone',
    description: 'Celebrating the top craft beers of the festival.'
  },
  {
    time: '8:30PM',
    title: 'Live music by The Broken Cymbal',
    icon: 'solar:music-notes-bold-duotone',
    description: 'Live performance to wrap up the evening vibes.'
  },
  {
    time: '11:30PM',
    title: 'Event ends',
    icon: 'solar:calendar-minimalistic-bold-duotone',
    description: ''
  }
])
</script>

<template>
  <div class="bg-background min-h-screen flex flex-col justify-between">
    <main class="mx-4 xl:mx-[60px] my-10 flex-grow">
      <h1 class="font-header text-primary text-center text-3xl md:text-4xl uppercase tracking-wider mb-8">
        Event Schedule
      </h1>

      <div class="bg-card rounded-xl p-4 md:p-4 w-full mx-auto flex flex-col gap-4">
        
        <div 
          v-for="(event, index) in scheduleEvents" 
          :key="index"
          @click="event.description && toggleDescription(index)"
          :class="[
            event.description ? 'cursor-pointer hover:bg-neutral-50' : '',
            'bg-white rounded-lg p-5 shadow-xs flex flex-col gap-4 transition-colors'
          ]"
        >
          <div class="flex items-center justify-between w-full">
            <div class="flex items-center gap-4">
              <Icon :name="event.icon" size="32px" class="text-primary flex-shrink-0" />
              <h2 class="font-header text-header text-lg md:text-xl">
                {{ event.title }}
              </h2>
            </div>
            <span class="font-header text-header text-lg md:text-xl whitespace-nowrap">
              {{ event.time }}
            </span>
          </div>

          <div 
            v-if="event.description && activeIndex === index" 
            class="bg-card rounded-lg p-4 text-context text-sm leading-relaxed font-primary"
          >
            {{ event.description }}
          </div>
        </div>

      </div>
    </main>

    <footer class="bg-primary text-text-accent text-center py-4 text-xs md:text-sm font-primary mt-12">
      © CBAC — Cambodian Craft Beer Association • Event: 16 August 2025 • Botanico Craft Beer Garden
    </footer>
  </div>
</template>