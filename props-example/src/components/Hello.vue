<template>
<div>
    <h1> {{ 'Ola' + ' ' + pessoa.nome }} </h1>
    <input type="text" v-model="dados">
    <p> {{ dados }} </p>
    <button @click="disable" :disabled="disableButton">Disable Me</button>
    <input type="text" @input="printInputMessage">
    <p>A mensagem de input eh {{ inputMessage }}</p>
</div>
</template>

<script>

export default {
 data(){
    return {
        disableButton: false,
        dados: '',
        inputMessage: 'true'
    }
 },
 props: {
    pessoa: {type: Object, required: true}
 },
 methods: {
    disable() {
        this.disableButton = true
    },
    printInputMessage(value){
        if (value != '') {
            this.inputMessage = 'false'
        }
    },
 },
}
</script>

<style>

</style>
