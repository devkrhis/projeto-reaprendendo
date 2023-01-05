<template>
    <div id="contadorMagico">
        <h2> O valor é: {{ valueMagic }}</h2>
        <h2> O valor Negativo é: {{ oldValue }}</h2>
        
    </div>
    
</template>

<script>
export default {
    props: ['valueMagic','oldValue']
    // também podemos realizar da seguinte forma:
    // props: [
    //     valueMagic: [ -> aqui eu transformo em um objeto
    //         type: String, -> passando o tipo, dizendo que é string
    //         required: true, -> forçando a ter, dizendo que tem que ter esse valueMagic
    //         default: "anonimo" -> aqui é caso não tenha nada, ai por padrão vai pegar anonimo
    //     ]
    // ]
    
}
</script>

<style scoped>

</style>