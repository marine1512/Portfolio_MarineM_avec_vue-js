<script>
/* importation et utilisation de la bibliothèque Email.js */
import emailjs from "@emailjs/browser";
export default{
  methods:{
      sendEmail() {
      emailjs.sendForm('service_5id4fcn', 'template_nhkdcg9', this.$refs.form, {
      publicKey: 'ic6YSvJuTWnMUU3AY',
      objet: "",
      message: "",
      LastName:"",
      name: "",
      })
        .then((Response)=> {
            console.log('SUCCESS!', Response);
            alert('Message bien envoyé !')
          },
          (error) => {
            console.log('FAILED...', error);
          },
        );
      },
    },
};
</script>

<template>
  <div id="contact">
     <h1>Contactez-moi !</h1>
      <form ref="form" @submit.prevent="sendEmail">
          <label for="name" >Nom:</label>
          <input id="name" type="text" name="name">
          <label for="LastName" >Prénom:</label>
          <input id="LastName" type="text" name="LastName">
          <label for="objet">Objet:</label>
          <input id="objet" type="text" name="objet"></input>
          <label for="message">Message:</label>
          <textarea id="message" name="message"></textarea>
          <div id="btn">
              <button type="submit">Envoyer</button>  
          </div>
      </form>
  </div>
</template>

<style scoped>
#contact{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 2em;
}
form{
  display: flex;
  flex-direction: column;
  color: #6d6e5c;
    margin-top: 2em;
  }
  h1{
    border-bottom: 0.1em solid #6d6e5c;
    width: fit-content;
    color: #6d6e5c;
    margin-top: 2em;
  }

  form>div{
    margin: 1em;
  }
  form>div>label{
    color: #a19f86;
    margin: 1em;
  }
  #btn{
    display: flex;
    justify-content: center;
  }
  button{
    background-color: #a19f86;
    color: white;
  }
</style>