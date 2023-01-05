<template>
    <div id="usuario">
        <h1> Controle de Usuário: {{ name }}</h1>
        <button type="button" @click="changeName"> Change Name </button>
        <hr>
        <segundoComponenteExportado :valueMagic="valueMagic" :oldValue='oldValue'/>
        <button type="button" @click="changeValue"> Change Value </button>
        <button type="button" @click="changeMenorValue"> Diminuindo Valor</button>

    </div>
    
</template>

<script>

import segundoComponenteExportado from './segundoComponenteExportado.vue';

export default {
    components: {
        segundoComponenteExportado
    },
    data(){
        return{
            name: 'Krhistopher',
            valueMagic: 0,
            oldValue: 100
        }
    },
    methods: {
        changeName(){
                this.name = 'Lucas'
            },
        changeValue(){
            this.valueMagic++

        },
        changeMenorValue(){
            this.oldValue--
        }
    }
    
}
</script>

<style scoped>

</style>