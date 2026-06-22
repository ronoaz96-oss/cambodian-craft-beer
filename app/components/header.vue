<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>

<template>
      <nav class="font-header bg-background relative z-50">

            <div class="flex items-center justify-between">
                  <div class="flex items-center gap-2">
                        <img src="/assets/images/logo1.png" alt="logo1" class="h-12 md:h-15">
                        <img src="/assets/images/logo2.png" alt="logo2" class="h-12 md:h-15">
                  </div>
      
                  <button @click="isOpen = !isOpen" class="xl:hidden p-2 text-primary">
                        <Icon :name="isOpen ? 'solar:close-circle-bold-duotone' : 'solar:hamburger-menu-bold-duotone'" size="25px" />
                  </button>
                  <div :class="[isOpen ? 'flex' : 'hidden', 'xl:flex absolute xl:relative top-full left-0 w-full xl:w-auto bg-background xl:bg-transparent flex-col xl:flex-row items-stretch xl:items-center border-b xl:border-none border-background']">
                        <NuxtLink to="/" class="nav"> 
                              <Icon name="solar:home-angle-2-bold-duotone" size="25px" class="text-primary icon" /> Home
                        </NuxtLink>
                        <NuxtLink to="/" class="nav">
                              <Icon name="solar:buildings-2-bold-duotone" size="25px" class="text-primary icon" /> Breweries
                        </NuxtLink>
                        <NuxtLink to="/" class="nav">
                              <Icon name="solar:calendar-minimalistic-bold-duotone" size="25px" class="text-primary icon" /> Schedule
                        </NuxtLink>
                        <NuxtLink to="/" class="nav">
                              <Icon name="solar:cup-hot-bold-duotone" size="25px" class="text-primary icon" /> Beer Style
                        </NuxtLink>
                        <NuxtLink to="/" class="nav">
                              <Icon name="solar:medal-ribbons-star-bold-duotone" size="25px" class="text-primary icon" /> Award
                        </NuxtLink>
                        <NuxtLink to="/" class="nav">
                              <Icon name="solar:users-group-two-rounded-bold-duotone" size="25px" class="text-primary icon" /> Sponsor
                        </NuxtLink>
                  </div>
                  <div class="hidden xl:flex text-[16px] bg-primary hover:bg-accent text-text-accent px-[15px] py-[25px] items-center justify-center">
                        <NuxtLink to="/">Judge Here</NuxtLink>
                  </div>
            </div>
      </nav>
</template>

<style scoped> 
.nav {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 25px 15px;
      font-size: 13px;
      transition: all 0.2s;
}

@media (max-width: 1280px) {
      .nav {
            padding: 15px 20px;
            justify-content: flex-start;
      }
}

.nav:hover {
      background-color: var(--color-primary);
      color: var(--color-text-accent);
}

.nav:hover .icon {
      color: var(--color-text-accent) !important;
}


</style>