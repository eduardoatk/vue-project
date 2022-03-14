<template>
    <!-- : abaixo é a forma reduzida de escrever v-bind -->
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="trocarImagem" />
    <!-- <Reutilizacao /> -->
</template>

<script>
import Reutilizacao from "./Reutilizacao.vue"
import MudarImagem from "./MudarImagem.vue"

export default {
    name: "Picture",
    components: {
        Reutilizacao,
        MudarImagem
    },
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: "Matheus Battisti"
        }
    },
    methods: {
        trocarImagem() {
            this.avatar = './img/avatar2.png'
        }
    }
}
</script>