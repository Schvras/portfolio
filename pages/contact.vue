<template>
    <div class="container mx-auto">
        <h1 class="text-4xl font-bold text-blue-600">Contatos</h1>
        <hr class="h-px my-8 bg-gray-200 border-0 dark:bg-gray-700">
        <div class="mt-3">
            <p>
                <a href="https://www.linkedin.com/in/jean-henrique-schvartz-92940a180/" target="_blank"
                    class="inline-flex items-center justify-center p-5 text-base font-medium text-gray-600 rounded-lg bg-gray-100 hover:text-gray-900 hover:bg-gray-200 dark:text-gray-400 dark:bg-gray-800 dark:hover:bg-gray-700 dark:hover:text-white">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/LinkedIn_icon.svg/2048px-LinkedIn_icon.svg.png"
                        alt="Linkedin" width="20">
                    <span class="ml-3 w-full">Entrar em contato via LinkdIn</span>
                    <svg class="w-4 h-4 ms-2 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                        fill="none" viewBox="0 0 14 10">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M1 5h12m0 0L9 1m4 4L9 9" />
                    </svg>
                </a>
            </p>

            <p class="mt-3">
                <a href="henrique.jeanschvartz@gmail.com" @click="copyURL"
                    class="inline-flex items-center justify-center p-5 text-base font-medium text-gray-600 rounded-lg bg-gray-100 hover:text-gray-900 hover:bg-gray-200 dark:text-gray-400 dark:bg-gray-800 dark:hover:bg-gray-700 dark:hover:text-white">
                    <img src="https://cdn-icons-png.flaticon.com/512/281/281769.png" alt="Gmail" width="20">
                    <span class="ml-3 w-full mr-3">Copiar e-mail henrique.jeanschvartz@gmail.com</span>
                    <img src="https://www.svgrepo.com/download/513766/copy.svg" alt="Copiar" width="30">
                </a>
            </p>
        </div>
    </div>
</template>


<script>
export default {
    methods: {
        async copyURL(e) {
            e.preventDefault();

            try {
                console.log(e)
                await navigator.clipboard.writeText(e.target.getAttribute('href'));
                window.alert('Copiado');
            } catch ($e) {
                window.alert('Não foi possível copiar');
            }
        }
    },
}
</script>