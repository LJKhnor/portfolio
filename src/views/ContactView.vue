<template>
  <div v-if="!emailSuccessfulySend" class="contact-view">
    <form
      id="myForm"
      action="mailto:lejeune.joachim@gmail.com"
      method="post"
      enctype="text/plain"
    >
      <ul>
        <li>
          <label for="name">Nom : </label>
          <input type="text" id="name" name="user_name" />
        </li>
        <li>
          <label for="mail">E-mail : </label>
          <input type="email" id="mail" name="user_mail" />
        </li>
        <li>
          <label for="msg">Message : </label>
          <textarea id="msg" name="user_message"></textarea>
        </li>
      </ul>
      <div class="button">
        <input
          type="submit"
          class="btn patient-record-validation"
          value="Send"
          @click.prevent="send()"
        />
      </div>
    </form>
  </div>
  <div v-if="emailSuccessfulySend" class="email-send-validation">
    <div class="validation-text">Email successfuly send</div>
    <div class="button return-home-button">
      <input
        type="submit"
        class="btn"
        value="Home"
        @click.prevent="backHome()"
      />
    </div>
  </div>
</template>
<script lang="ts">
import { ref } from 'vue'
import emailjs from '@emailjs/browser'
import router from '@/router'
export default {
  name: 'ContactView',
  setup() {
    const emailSuccessfulySend = ref(false)
    function initEmailJs() {
      emailjs.init({
        publicKey: '-cEDF_uJE7BZZsg2h',
      })
    }
    function send() {
      initEmailJs()
      emailjs.sendForm('service_5xf0hek', 'template_m58wj0f', '#myForm').then(
        () => {
          console.log('SUCCESS sending email !')
          emailSuccessfulySend.value = true
        },
        (error: string) => console.error('FAILED sending email...', error),
      )
    }
    function backHome() {
      router.push('/')
    }
    return { emailSuccessfulySend, send, backHome }
  },
}
</script>
<style>
.contact-view {
  position: relative;
  margin: 10vh;
}
form {
  /* On centre le formulaire */
  margin: 0 auto;
  width: 60vh;
  /* Le contour du formulaire */
  padding: 1em;
  border: 4px solid var(--color-border);
  border-radius: 1em;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
form li + li {
  margin-top: 1em;
}

label {
  /* Taille et alignement uniformes */
  display: inline-block;
  width: 20vh;
  color: var(--color-theme);
}
input,
textarea {
  /* On s'assure que les champs texte ont la même police
     Par défaut, les zones de texte ont une police à chasse
     fixe. */
  font: 1em sans-serif;

  /* Taille uniforme pour des champs */
  width: 35vh;
  box-sizing: border-box;

  /* On utilise la même bordure que pour le formulaire */
  border: 1px solid var(--color-border);
}

input:focus,
textarea:focus {
  /* On rajoute une mise en avant pour les éléments avec
     le focus. */
  border-color: var(--color-theme);
}
textarea {
  /* On aligne les textes sur plusieurs lignes avec leur
     libellé. */
  vertical-align: top;

  /* On fournit un peut d'espace pour saisir du texte. */
  height: 10em;

  /* On permet de redimensionner verticalement. */
  resize: vertical;
}
.button {
  margin-top: 2vh;
  text-align: center;
}
.btn {
  width: 20vh;
  background-color: var(--color-theme);
  cursor: pointer;
  border-radius: 30px;
}
.btn:hover {
  box-shadow: 0 0 12px 4px var(--color-theme-fade);
}
@media (max-width: 750px) {
  form {
    /* On centre le formulaire */
    margin: 0 auto;
    width: calc(100% - 10vh);
    /* Le contour du formulaire */
    padding: 1em;
    border: 4px solid var(--color-border);
    border-radius: 1em;
  }
  label {
    width: 10vh;
  }
  input,
  textarea {
    /* On s'assure que les champs texte ont la même police
     Par défaut, les zones de texte ont une police à chasse
     fixe. */
    font: 1em sans-serif;

    /* Taille uniforme pour des champs */
    width: calc(100% - 2px);
    box-sizing: border-box;

    /* On utilise la même bordure que pour le formulaire */
    border: 1px solid var(--color-border);
  }
}
</style>
