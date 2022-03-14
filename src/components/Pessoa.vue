<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email" :estaTrabalhando="true" />
        <Form />
    </div>
</template>

<script>
import Info from "./Info.vue"
import Form from "./Form.vue"

export default {
    nome: "Pessoa",
    components: {
        Info,
        Form
    },
    data() {
        return {
            nome: "Matheus",
            email: "matheus@email.com"
        }
    }
}
</script>
