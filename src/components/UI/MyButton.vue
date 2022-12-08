<template>
  <button class="button">
<slot></slot>
  </button>
</template>

<script>
export default {
name: 'my-button'
}
</script>

<style scoped>
.button {
  margin: 10px auto;
  display: flex;
  border: 2px solid teal;
  border-radius: 5px;
  color: slategrey;
  transition: 0.3s;
  cursor: pointer;
}

.button:hover {
  background-color: rgb(232, 105, 36);
}

.button:active{
  filter: brightness(70%);
}
</style>

