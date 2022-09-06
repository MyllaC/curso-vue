<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizado as seguintes tecnologias</p>
    <ul>
      <li>JavaScript</li>
      <li>Java</li>
      <li>React</li>
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">
      Para acessar meu portfólio
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture.vue";
export default {
  name: "Info",
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: "criscamila09@gmail.com",
      meu_link: "https://github.com/MyllaC",
      textoBotao: "Mostrar e-mail",
    };
  },
  components: { Picture },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textoBotao = "Mostrar e-mail";
      } else {
        this.textoBotao = "Ocultar e-mail";
      }
    },
  },
};
</script>

<style>
.paragrafo-pai {
  color: red;
}
</style>
