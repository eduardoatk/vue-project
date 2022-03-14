<template>
    <div>
        <p v-if="estaTrabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades.</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li
                v-for="(technology, index) in backend_technologies"
                v-bind:key="index"
            >{{ technology }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li
                v-for="technologies in frontend_technologies"
                :key="technologies.id"
            >{{ technologies.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrarEmail">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">
            Para acessar meu portfólio basta
            <a v-bind:href="meu_link" target="_blank">clicar aqui</a>
        </p>
        <Picture />
    </div>
</template>

<script>
import Picture from "./Picture.vue"

export default {
    name: "Info",
    components: {
        Picture
    },
    props: {
        email: String,
        estaTrabalhando: Boolean
    },
    data() {
        return {
            mostrarEmail: false,
            meu_link: "https://google.com",
            textoBotao: "Mostrar e-mail",
            backend_technologies: ["Javascript", "PHP", "Python"],
            frontend_technologies: [
                { id: 1, language: "HTML" },
                { id: 1, language: "CSS" },
                { id: 1, language: "Vue" }
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrarEmail = !this.mostrarEmail
            if (!this.mostrarEmail) {
                this.textoBotao = "Mostrar e-mail"
            } else {
                this.textoBotao = "Esconder e-mail"
            }
        }
    }
}
</script>

<style>
.paragrafo-pai {
    color: red;
}
</style>