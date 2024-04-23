<template>
    <div id="modal" v-if="props.isOpen">
    <div id="modal-wrapper">
    <div id="modal-content">
        <slot name="body"></slot>
    </div>
    </div>
    </div>
  </template>

<script setup>

const props = defineProps ({isOpen:Boolean})
</script>

<style scoped>
#modal{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);

}
#modal-wrapper{
    display: flex;
    justify-content: end;
    height: 100%;
}
#modal-content{
    background-color: #daccc7;
    border: 0.3em solid #6d6e5c;
    color: black;
    padding: 20px 30px;
}
</style>