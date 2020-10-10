<script>
export default {
  name: 'BaseInputText',
  props: {
      fromPropValue: {
        type: String,
        default: ''
      }
  }
}
</script>

<template>
  <input
    type="text"
    class="input"
    :value="fromPropValue"
    @keydown.enter="e => $emit('inputtext', e.target.value)"
  >
  
</template>

<style>

</style>