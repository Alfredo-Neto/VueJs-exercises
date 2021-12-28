<template>
  <div>
    <meu-hello :pessoas="pessoas"></meu-hello>
  </div>
</template>

<script>

import MeuHello from '@/components/Hellos.vue'
export default {
  components: {
    MeuHello
  },
  data(){
    return {
      pessoas: [
        {nome: 'Alfredo'},
        {nome: 'Jorge'},
        {nome: 'Alexandre'},
        {nome: 'Marcio'},
      ],
    }
  },
}
</script>

<style>

</style>
