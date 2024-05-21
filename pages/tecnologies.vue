<template>
    <div class="container mx-auto">
        <h1 class="text-4xl font-bold text-blue-600">Tecnologias</h1>
        <hr class="h-px my-8 bg-gray-200 border-0 dark:bg-gray-700">
        <div class="mt-3">

            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
                <div v-for="(tecnologia, index) in tecnologias" :key="index"
                    class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
                    <h2 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ tecnologia.nome
                        }}</h2>
                    <h3 class="mb-2 text-lg font-semibold text-gray-900 dark:text-white">Projetos:</h3>
                    <p v-if="tecnologia.projetos.length <= 0" class="text-gray-400">Nenhum projeto citado.</p>
                    <ul v-for="(projeto, projetoIndex) in tecnologia.projetos" :key="projetoIndex"
                        class="max-w-md space-y-1 text-gray-500 list-disc list-inside dark:text-gray-400">
                        <li>
                            <a target="_blank" :href="projeto.link" class="text-blue-600 hover:underline">{{ projeto.nome }}
                            </a>
                        </li>
                    </ul>

                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            tecnologias: []
        };
    },
    async mounted() {
        try {
            const response = await fetch('/tecnologias.json');
            if (!response.ok) {
                throw new Error('Erro ao carregar dados.');
            }
            this.tecnologias = await response.json();
        } catch (error) {
            console.error(error);
        }
    }
}
</script>

<style>
/* Estilos adicionais podem ser adicionados aqui */
</style>