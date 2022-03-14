<template>
    <div>
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue"
import Reutilizacao from "./Reutilizacao.vue"

export default {
    name: 'App',
    components: {
    MultiplosEventos,
    Reutilizacao
},
    data() {
        return {
            nome: "Matheus",
            profissao: "programador"
        }
    }
}
</script>
