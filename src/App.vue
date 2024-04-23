<script setup>
/* import des commposants visible sur toutes les pages */
import { RouterLink, RouterView } from 'vue-router'
import Logo from "@/components/header.vue"
import Bottom from '@/components/footer.vue'


</script>

<template>
    <Logo></Logo>
    <RouterView />
    <Bottom></Bottom>

</template>

<style scoped>
</style>