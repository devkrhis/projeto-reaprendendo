<template>
    <div id="alterandoNome">
        <h1> Bem vindo ao Glossário </h1>
        <h2> Seu nome está: {{ name }}</h2>
        <button type="button" @click="recoverName"> Reiniciando Nome </button>
        <button type="button" @click="secondAvaliation">  Validar Novamente CPF </button>
        <button type="button" @click="thirdAvalatiation">  Ultima Checkagem </button>
    </div>
    
</template>

<script>
/* eslint-disable */
export default {
    props: ['name', 'orgDevedor'],
    methods: {
        recoverName(){
            this.name = 'Krhistopher'
            this.$emit('alteracaoDeNome', this.name)
        },
        secondAvaliation(){
            this.orgDevedor = 'O seu nome está sujo'
            this.$emit('VerificandoCpf', this.orgDevedor)
        },
        thirdAvalatiation(){
            this.orgDevedor = 'Está limpo'
            this.$emit('VerificandoNovamenteCpf', this.orgDevedor)
        }
    }
    
}
</script>

<style scoped>

</style>