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
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
  </div>
</template>

<script>
export default {
  name: "Info",
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: "criscamila09@gmail.com",
    };
  },
};
</script>
