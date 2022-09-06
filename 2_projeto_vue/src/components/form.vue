<template>
  <div class="form">
    <h2>Meu formulário</h2>
    <form action="" @submit="enviarFormulario($event)">
      <!--
        <div><InputText /></div>
        <div><InputText /></div>
      -->
      <div>
        <input type="text" v-model="name" />
      </div>
      <div>
        <input type="text" v-model="email" />
      </div>
      <div><Submit /></div>
    </form>
  </div>
</template>

<script>
import InputText from "./form/InputText.vue";
import Submit from "./form/Submit.vue";
export default {
  name: "Form",
  components: { InputText, Submit },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("Formulario enviado");
      console.log(`Nome: ${name} Email: ${email}`);

      //Ajax para mandar os dados para o banco de dados
    },
  },
};
</script>

<style scoped>
.form {
  padding-bottom: 100px;
}
</style>
