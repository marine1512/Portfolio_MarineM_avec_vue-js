<script setup>
</script>

<template>
    <div id="bottom">
      <div id="img">
        <a href="https://github.com/marine1512"><img src="../assets/Logo_Github.png" alt="GitHub"></a>
        <a href="https://www.linkedin.com/in/marine-mignot-89b732140/"><img src="../assets/Logo_Linkedin.png" alt="LinkedIn"></a>
        <a href="https://twitter.com"><img src="../assets/Logo_Twitter.png" alt="Twitter"></a>
        <a href="https://www.facebook.com"><img src="../assets/Logo_Facebook.png" alt="Facebook"></a>
        <a href="https://www.instagram.com"><img src="../assets/Logo_Instagram.png" alt="Instagram"></a>
      </div>
      <div id="maj">
        <p>Mise a jour le 23 avril 2024</p>
      </div>
    </div>
</template>

<style scoped>
#bottom{
  background-color: #776a7e;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1em;
}
#img>a>img{
  width: 2em;
  margin-right: 1em;
  cursor: pointer;

}
#img>a>img:hover{
  font-size: 1.2rem;
  transition: 0.3s;
}


</style>