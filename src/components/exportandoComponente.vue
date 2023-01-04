<template>
    <div id="usuario">
        <h1> Controle de Usuário: {{ name }}</h1>
        <button type="button" @click="changeName"> Change Name </button>
    </div>
    
</template>

<script>
export default {
    data(){
        return{
            name: 'Krhistopher',
        }
    },
    methods: {
        changeName(){
                this.name = 'Lucas'
            }
    }
    
}
</script>

<style scoped>

</style>