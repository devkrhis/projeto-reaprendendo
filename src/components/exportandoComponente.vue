<template>
    <div id="usuario">
        <h1> Controle de Usuário: {{ name }}</h1>
        <button type="button" @click="changeName"> Change Name </button>
        <hr>
        <segundoComponenteExportado :valueMagic="valueMagic" :oldValue='oldValue'/>
        <button type="button" @click="changeValue"> Change Value </button>
        <button type="button" @click="changeMenorValue"> Diminuindo Valor</button>
        <hr>
        <hr>
        <reinicializandoNome :name="name" @alteracaoDeNome="name = $event" @VerificandoCpf="orgDevedor = $event" @VerificandoNovamenteCpf="orgDevedor = $event"/>

        <div id="cadastro">
            <hr>
                <h2> Situação do Cadastro</h2>
                <button type="button" @click="changeOption"> Verificar Informações </button>
                <template v-if="optionValue == true">
                    <h3> Regularizado: {{ regular }} </h3>
                    <h3> SPC: {{ spc }} </h3>
                    Orgão devedor <strong>{{ orgDevedor }}</strong>
                </template>
            <hr>
            <button type="button" @click="reiniciarInfo"> Reiniciar Informações </button>
        </div>
    </div>
    
</template>

<script>

import segundoComponenteExportado from './segundoComponenteExportado.vue';
import reinicializandoNome from './reinicializandoNome.vue';

export default {
    components: {
        segundoComponenteExportado,
        reinicializandoNome
    },
    data(){
        return{
            name: 'Krhistopher',
            valueMagic: 0,
            oldValue: 100,
            matricula: 'Indisponivel',
            regular: 'Sim',
            spc: 'Não',
            orgDevedor: 'Não foi possível analisar',
            optionValue: false
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
        },
        changeOption(){
            this.optionValue = true
        },
        reiniciarInfo(){
            this.orgDevedor = 'Não foi possível analisar'
        }
    }
    
}
</script>

<style scoped>

</style>