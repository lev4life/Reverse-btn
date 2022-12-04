<template>
  <input :value="value" @input="updateInput" class="input" type="text">
</template>

<script>
export default {
name: 'my-input',
props: {
  value: [String, Number]
},
methods: {
  updateInput(event) {
    this.$emit('update:value', event.target.value)
  }
}
}
</script>

<style scoped>

.input {
  width: 20%;
  margin: 0 auto;
  display: flex;
  border: 2px solid teal;
  border-radius: 5px;
  color: slategrey;
}

</style>