<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info />
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
    };
  },
  components: { Info, Form },
};
</script>
