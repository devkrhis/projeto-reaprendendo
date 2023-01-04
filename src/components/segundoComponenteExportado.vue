<template>
    <div id="contadorMagico">
        <h2> O valor é: {{ valueMagic }}</h2>
        <h2> O valor Negativo é: {{ oldValue }}</h2>
        
    </div>
    
</template>

<script>
export default {
    props: ['valueMagic','oldValue']
    
}
</script>

<style scoped>

</style>