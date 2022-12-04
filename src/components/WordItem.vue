<template>
  <div class="revert">
    <div>
      <div class="result">Элемент: {{ reverse(revert.revertWord) }}</div>
      <div class="revert__btns">
        <my-button @click="$emit('remove', revert)" >Удалить</my-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    revert: {
      type: Object,
      required: true,
    },
  },
  methods: {
    reverse: (string) => {
      let result = "";

      for (let i = string.length - 1; i >= 0; i--) {
        result += string[i];
      }

      return result;
    },
  },
};
</script>

<style>
.result {
  width: 20%;
  margin: 10px auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border: 2px solid teal;
  border-radius: 5px;
  color: slategrey;
}
</style>
