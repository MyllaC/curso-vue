<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <Reutilizacao />
  </div>
</template>

<script>
import Reutilizacao from "./Reutilizacao.vue";
export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Imagem de login",
    };
  },
  components: { Reutilizacao },
};
</script>
