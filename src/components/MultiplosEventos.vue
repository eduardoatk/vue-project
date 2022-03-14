<template>
    <div>
        <!-- DUAS FORMAS DE CHAMAR O EVENTO: -->
        <button @click="primeiro($event), segundo(texto, $event)">Ativar múltiplos eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>

<script>
export default {
    name: "MultiplosEventos",
    data() {
        return {
            multiplos_eventos: "",
            texto: "Segundo evento!"
        }
    },
    methods: {
        primeiro(e) {
            this.multiplos_eventos = "Primeiro evento ativado!";
        },
        segundo(txt, e) {
            setTimeout(() => this.multiplos_eventos = txt, 1500)
        }
    }
}
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>