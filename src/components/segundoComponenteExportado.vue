<template>
    <div id="contadorMagico">
        <h2> O valor é: {{ valueMagic }}</h2>
        <h2> O valor Negativo é: {{ oldValue }}</h2>
        <hr>
        <h1> Situação do Aluno: {{ matricula }} </h1>
        <button type="button" @click="changeSituation"> Change Matricula </button>
        
    </div>
    
</template>

<script>
export default {
    /* eslint-disable */
    // props: ['valueMagic','oldValue']
    // também podemos realizar da seguinte forma:
    props: { // -> aqui vira um objeto também
        valueMagic: { //-> aqui eu transformo em um objeto
            type: Number, //-> passando o tipo, dizendo que é string
            // required: true, //-> forçando a ter, dizendo que tem que ter esse valueMagic
            default: 100 //-> aqui é caso não tenha nada, ai por padrão vai pegar anonimo ou o que eu coloquei.
        },
        oldValue: {
            type: Number // mesmo funcionando ele apresenta erro no console, pois tenta fazer a verificação
        },
        matricula: {
            type: String,
            default: 'Matricula'
        }
    },
    methods: {
        changeSituation(){
            this.matricula = "Disponivel"
        }
    }
    
}
</script>

<style scoped>

</style>