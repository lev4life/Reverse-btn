<template>
    <h1 class="resultTitle">Результат:</h1>
    <div v-if="(reverts.length > 0)">
        <word-item 
        v-for="revert in reverts"
        :revert="revert"
        :key="revert.id"
        @remove="$emit('remove', revert)"
        />
    </div>
    <h2 v-else class="smallTitle" >Список пуст. Добавьте элемент.</h2>

</template>

<script>
import WordItem from '@/components/WordItem.vue'
export default {
  components: { WordItem },
    props: ['reverts']
    
    
}
</script>

<style scoped>
.resultTitle {
    text-align: center;
  margin-top: 100px;
  color: slategrey;
}

.smallTitle {
    text-align: center;
  margin-top: 10px;
  color: slategrey;
}
</style>