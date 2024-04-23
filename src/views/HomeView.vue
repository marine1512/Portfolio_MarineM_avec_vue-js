<script setup>
import Presentation from '@/components/presentation.vue'
import Crea from '@/components/crea.vue'
import Contact from '@/components/contact.vue'
import Modal from '@/components/Modal.vue';

</script>

<template>
  <main>
    <a href="#logo"><img id="top" src="@/assets/top.png" alt="haut de la page"></a>
    <Presentation></Presentation>
    <Crea></Crea>
    <Modal></Modal>
    <Contact></Contact>
  </main>
</template>

<style>
main{
  position: relative;
}
#top{
  width: 3em;
    background-color: #b5a5c7;
    opacity: 70%;
    position: fixed;
    right: 1em;
    bottom: 1em;
}
</style>
