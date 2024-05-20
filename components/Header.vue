<template>
  <nav class="bg-gray-800 p-4">
    <div class="container mx-auto flex justify-between items-center">
      <div class="flex items-center">
        <span class="text-white text-xl font-semibold">Portfólio</span>
        <ul :class="{ 'hidden': !isMenuOpen }" class="ml-4 flex items-center space-x-4">
          <li>
            <NuxtLink to="/" class="text-white hover:text-gray-300">Início</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about" class="text-white hover:text-gray-300">Sobre</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/skills" class="text-white hover:text-gray-300">Habilidades</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/projects" class="text-white hover:text-gray-300">Projetos</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/contact" class="text-white hover:text-gray-300">Contato</NuxtLink>
          </li>
        </ul>
      </div>
      <div>
        <button @click="toggleMenu" class="text-white hover:text-gray-300 focus:outline-none md:hidden">
          <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path :class="{ 'hidden': isMenuOpen }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
            <path :class="{ 'hidden': !isMenuOpen }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
      </div>
    </div>
  </nav>
</template>


<script>
export default {
  data() {
    return {
      isMenuOpen: true
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
}
</script>

<style scoped>
/* Estilos específicos do componente */
</style>