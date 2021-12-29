<template>
  <button :class="baseClass">
    <slot />
  </button>    
</template>

<script>
export default {
  /**
   * regra geral(porem flexivel): usar props quando queremos alterar o comportamento do elemento
   * usar slot quando queremos alterar o conteudo do elemento
   * Exemplo no arquivo SlotExample.vue
   */
  props: {
    title: {
        type: String, 
        default: 'Button', 
    },

    variant: {
        type: String,
        default: 'primary'
    },
  },

  computed: {
    baseClass() {
        return [
            'btn',
            this.getVariant
        ]
    },

    getVariant() {
        return this.variant ? `btn-${this.variant}` : ''
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
