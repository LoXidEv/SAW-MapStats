<script setup>
import MapTiled from '@/components/MapTiled.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
    <main>
        <MapTiled />
    </main>
    <Footer />
</template>

<style scoped>
main {
    position: relative;
    width: 100vw;
    height: 100vh;
    margin: 0;
    padding: 0;
    overflow: hidden;
}
</style>
