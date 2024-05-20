<template>
    <footer class="bg-gray-800 text-white py-4 text-center fixed bottom-0 w-full">
      <p>&copy; 2024 {{ author }}</p>
    </footer>
</template>

<script>
import { author } from '~/static/data'
</script>


<script>
import data from '~/static/data';

export default {
    data: function (){
        return {
            author: data.author
        }
    },
}
</script>