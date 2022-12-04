<template>
  <form @submit.prevent>
      <h1 class="title">Текст задом наперед!</h1>
      <my-input
        v-model:value="revert.revertWord"
        type="text"
        placeholder="Введите текст..."
      />
      <my-button class="button"

      @click="createRev"
    

      >Обратить!</my-button>
      
    </form>
    
</template>

<script>

export default {
    
data() {
    return {
        revert: {
            revertWord: '',


        }
    }
},
methods: {
    createRev() {
        this.revert.id = Date.now();
        this.$emit('create', this.revert)
        this.revert = {
            revertWord: '',
        }
    },
}
}
</script>

<style scoped>
.title {
  text-align: center;
  margin-top: 200px;
  color: slategrey;
}

</style>