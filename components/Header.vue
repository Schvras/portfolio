<template>
    <nav class="bg-gray-800 p-4">
      <div class="container mx-auto flex justify-between items-center">
        <div class="flex items-center">
          <NuxtLink to="/" class="text-white hover:text-gray-300"><span class="text-white text-xl font-semibold">Jean H Schvartz</span></NuxtLink>
          <ul class="ml-4 flex items-center space-x-4">
            <li>
              <NuxtLink to="/" class="text-white hover:text-gray-300">Início</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" class="text-white hover:text-gray-300">Sobre</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/tecnologies" class="text-white hover:text-gray-300">Tecnologias</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/contact" class="text-white hover:text-gray-300">Contato</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </template>