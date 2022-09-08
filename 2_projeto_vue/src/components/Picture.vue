<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="handleMudarImagem" />
  </div>
</template>

<script>
import Reutilizacao from "./Reutilizacao.vue";
import MudarImagem from "./MudarImagem.vue";
export default {
  name: "Picture",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Imagem de login",
    };
  },
  methods: {
    handleMudarImagem() {
      this.avatar = "/img/avatar2.png";
    },
  },
  components: { Reutilizacao, MudarImagem },
};
</script>
