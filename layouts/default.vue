<template>
    <div>
        <div class="relative">
            <Header />

            <div class="container mx-auto py-8">
                <slot></slot>
            </div>

            <Footer />
        </div>
    </div>
</template>


<style scoped>
main{
    flex: 1;
}
</style>