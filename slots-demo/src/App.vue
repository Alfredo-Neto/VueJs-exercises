<template>
  <div class="container mt-10">
   <AppButton>
     <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
     Salvar
   </AppButton>
    <br>
    <br>
   <AppButton>
     Editar
   </AppButton>
    <br>
    <br>
   <SlotExample variant="success">
     Deletar
   </SlotExample>
  </div>
</template>

<script>

import AppButton from "@/components/AppButton.vue";
import SlotExample from "@/components/SlotExample.vue";
export default {
  components: {
    AppButton,
    SlotExample
  },
}
</script>

<style>

</style>
