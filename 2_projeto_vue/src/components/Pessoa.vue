<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando="true" />
    <Form />
  </div>
</template>

<script>
import Info from "./Info.vue";
import Form from "./form.vue";
export default {
  name: "Pessoa",
  data() {
    return {
      nome: "Camila",
      email: "criscami222a@gmail.com",
    };
  },
  components: { Info, Form },
};
</script>
