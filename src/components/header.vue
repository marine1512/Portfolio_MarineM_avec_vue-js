<script setup>
</script>

<template>
  <header>
      <div id="logo">
      <RouterLink to="/"><img id="image" src="../assets/Logo.jpeg" alt="Logo"></RouterLink>
      <h1>Marine</h1>
      <h1>Mignot</h1>
      <p>Developpeuse Web Junior</p>
      </div>
      <nav id="navbar">
          <ul>
            <li><a href="#presentation">Présentation</a></li>
            <li><a href="#crea">Créations</a></li>
            <li><a href="#contact">Contact</a></li>
            <RouterLink to="/no">Suite</RouterLink>
        </ul> 
    </nav>
  </header>    
</template>

<style scoped>
#logo{
  width: 100%;
  height: 27em;
  color: #41334e;
  background-color: #daccc7;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 2.5em;
}
#image{
  border-radius: 0 0 8em 0;
  border: 0.2em solid #b5a5c7;
  width: 16em;
  height: 21em;
}
#logo>p {
  margin: 1em 0 1em 0;
  position: relative;
  font-size: 1.2em;
  bottom: 3em;
  right: -8em;
}
#logo>h1{
  margin-top: 0.1em;
  margin-bottom: 0;
  position: relative;
  top: -2em;
  right: -6em;
  font-size: 1.5em;
}
#navbar>ul{
  padding: 1em;
  display: flex;
  justify-content: space-evenly;
  margin: 0;
  background-color: #b5a5c7;
  color: #daccc7;
  list-style: none;

}

a {
    color: antiquewhite;
    text-decoration: none;
}
nav ul li:hover {
    text-decoration: underline;
    font-size: 1.2rem;
    transition: 0.3s;
}
nav > ul> a:hover{
  text-decoration: underline;
  font-size: 1.2rem;
    transition: 0.3s;
}
</style>