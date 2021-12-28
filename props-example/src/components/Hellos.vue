<template>
    <div class="hello-pessoas">
        <hello 
        v-for="pessoa in pessoas" 
        :key="pessoa.nome"
        :pessoa="pessoa">
        </hello>
    </div>
</template>

<script>

import Hello from '@/components/Hello.vue'
export default {
 props: {
    pessoas: {type: Array, required: true}
 },
 components: {
    Hello
 },
}
</script>

<style>

</style>
