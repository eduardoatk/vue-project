<template>
    <form action="" @submit="enviarFormulario($event)">
        <div>
            <h2>Meu formulário</h2>
        </div>
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <Submit />
        </div>
    </form>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
</template>

<script>
    import InputText from "./Form/inputText.vue"
    import Submit from "./Form/Submit.vue"

    export default {
        name: "Form",
        components: {
            InputText,
            Submit
        },
        data() {
            return {
                name: "",
                email: ""
            }
        },
        methods: {
            enviarFormulario(e) {
                e.preventDefault();

                const name = this.name;
                const email = this.email;

                console.log("Formulário enviado!");
                console.log("O nome é " + name);
                console.log("O e-mail é " + email);

                // Ajax
                // Inserir no banco de dados
            }
        }
    }
</script>

<style scoped>
    h2 {
        margin: 10px 0 10px 0;
    }

    p {
        margin: 150px;
    }
</style>