<template>
  <div class="bg-gray-100 min-h-screen flex justify-center pt-3">
    <div class="container mx-auto">
      <h1 class="text-4xl font-bold text-blue-600">Meu portfólio</h1>
      <p class="text-lg text-gray-700 mt-4">Bem-vindo ao meu site! Eu sou Jean Henrique Schvartz.</p>
      <p class="text-lg text-gray-700 mt-4">
        <NuxtLink to="/about" class="text-blue hover:text-blue">Saiba mais!</NuxtLink>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
