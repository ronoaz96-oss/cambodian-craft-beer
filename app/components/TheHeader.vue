<template>
 

    <!-- Hidden checkbox -->
    <input type="checkbox" id="menu-toggle" class="hidden peer"/>

    <!-- Header -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white ">
      <div class="flex items-center justify-between px-2 pl-0 sm:px-6 lg:p h-14 md:h-25  mx-auto">

        <!-- Logo -->
        <a href="/" class="flex items-center gap-2 shrink-0">
          <img src="/image/logo.png" alt="Cambodian Craft" class="w-34 md:w-35">
        </a>

        <!-- Desktop / tablet nav -->
        <nav class="hidden md:flex lg:flex items-center sm:w-[640px] md:w-[760px] lg:w-385  text-2xl gap-8">
          <a href="/" class="text-gray-700 hover:text-indigo-600 font-medium transition-colors">Home</a>
          <a href="/products" class="text-gray-700 hover:text-indigo-600 font-medium transition-colors">Products</a>
          <a href="/about" class="text-gray-700 hover:text-indigo-600 font-medium transition-colors">About</a>
          <a href="/contact" class="text-gray-700 hover:text-indigo-600 font-medium transition-colors">Contact</a>
        </nav>

        <!-- Burger (mobile only) -->
        <label
            for="menu-toggle"
            class="burger md:!hidden p-2.5  rounded-lg text-gray-600  bg-red-100 active:bg-gray-200 transition-colors cursor-pointer"
            aria-label="Toggle menu"
          >
          <span></span>
          <span></span>
          <span></span>
        </label>
      </div>
    </header>

    <!-- Overlay (mobile only) -->
    <label
      for="menu-toggle"
      class="md:hidden fixed inset-0 z-40 bg-black/30 opacity-0 pointer-events-none transition-opacity duration-300
             peer-checked:opacity-100 peer-checked:pointer-events-auto"/>

    <!-- Slide-in from right nav (mobile only) -->
    <nav
      class="md:hidden  fixed top-14 right-0 bottom-0 pt-0 z-50 w-72 sm:w-80 bg-gray-50 shadow-xl
             translate-x-full transition-transform duration-300 ease-in-out 
             peer-checked:translate-x-0">
      <!-- Nav header -->
 

      <!-- Nav links -->
      <ul class="flex flex-col  divide-y divide-gray-50 ">
        <li>
          <label for="menu-toggle">
            <NuxtLink
                to="/home"
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '/home' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Home</span>
            </NuxtLink>
          </label>
        </li>
        <li>

          <NuxtLink
                to="...."
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '...' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Breweries</span>
            </NuxtLink>
        </li>
        <li>
          <NuxtLink
                to="...."
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '...' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Schedule</span>
            </NuxtLink>

        </li>
        <li>
          <NuxtLink
                to="...."
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '...' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Beer Style</span>
            </NuxtLink>
        </li>
        <li>
          <NuxtLink
                to="...."
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '...' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Award</span>
            </NuxtLink>
        </li>
        <li>
          <NuxtLink
                to="...."
                class="flex items-center gap-3 px-6 py-4 transition-colors
                       focus:outline-none focus:ring-2 focus:ring-[#800020]
                       active:scale-95"
                :class="route.path === '...' ? 'bg-[#800020] text-white' : 'text-[#800020] hover:bg-red-100'">
              <span class="font-bold">Sponsor</span>
            </NuxtLink>
        </li>
      </ul>
    </nav>

    

</template>

<script setup>
const route = useRoute()
</script>

<style scoped>
.burger {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 5px;
  width: 40px;
  height: 40px;
}
.burger span {
  display: block;
  height: 2px;
  width: 20px;
  background: currentColor;
  border-radius: 2px;
  transition: transform 0.3s ease, opacity 0.2s ease;
  transform-origin: center;
}
/* Animate to X when checked */
#menu-toggle:checked ~ header .burger span:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}
#menu-toggle:checked ~ header .burger span:nth-child(2) {
  opacity: 0;
  transform: scaleX(0);
}
#menu-toggle:checked ~ header .burger span:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}
</style>