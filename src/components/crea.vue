<script setup>
import { dataBase } from '@/stores/data'
import { onClickOutside } from '@vueuse/core'
import Modal from '@/components/Modal.vue';
import { onMounted , ref } from 'vue';


const info = ref(dataBase)
const info1 = ref(info.value[0])
const Tableau = ref([])
const paramClose = ref(null)
const validBool = ref(false)

onMounted (()=>{

  /* Création d'un tableau avec les données de chaque projets. En lien avec le fichier data.js */
    Tableau.value = dataBase
  /* Overlay et fermeture en cliquant n'importe où */
    onClickOutside(paramClose, closeModal)

})
/* Ouverture et fermeture de la modal */
const openModal = (project)=>{
    info1.value = project
    validBool.value = true
}
const closeModal = ()=>{
    validBool.value = false
}

</script>

<template>
  <section id="crea">
    <h1>Mes Créations</h1>
    <ul>
    <li v-for="project in Tableau" :key="project.id">
    <h2>{{ project.title }}</h2>
    <button @click="openModal(project)"><img :src="project.img" alt="Créations"></button>
    <Modal :isOpen="validBool">
      <template #body>
      <button @click="closeModal" id="btn">X</button>
      <h3>{{ info1.title }}</h3>
      <img :src="info1.img" alt="Créations" id="img-modal">
      <p>{{ info1.techno }}</p>
      <a v-bind:href="info1.lien" target="_blank">Lien du projet</a>
      <br>
      <a v-bind:href="info1.repository" target="_blank">Lien du repository</a>
      </template>
    </Modal>
    </li>
    </ul>
  </section>
</template>

<style scoped>
h1{
  color: #6d6e5c;
  text-decoration: underline;
  margin-bottom: 1em;
}
h2 {
    color: #a19f86;
}
h3{
  text-decoration: underline;
}
#crea{
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color:  #daccc7;
}
ul{
  list-style: none;
}
img{
  width: 28em;
  
}
button>img:hover{
  box-shadow: 13px 20px 8px 0px #6d6e5c;
}
#btn{
  background-color: red;
  color: antiquewhite;
  margin-right: 2em;
  position: relative;
  left: 32em;
}
#img-modal{
  border: 0.1em solid black;
}
a{
  text-decoration: none;
  color: black;
}
</style>