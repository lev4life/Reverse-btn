<template>
  <div class="app">
    <word-form
    @create="createRev"
    />
    <word-list 
    :reverts="reverts"
    @remove="removeRev"
    />
    
  </div>
</template>

<script>
import WordForm from "@/components/WordForm"
import WordList from "@/components/WordList"
export default {
    components: {
        WordForm, WordList
    },
data() {
    return {

        reverts: [
        
    ],

    }
},
methods: {
    createRev(revert) {
    this.reverts.push(revert);   
    },
    
    removeRev(revert) {
        this.reverts = this.reverts.filter(r => r.id !== revert.id)
  }
    
},


}
</script>

<style scoped>






</style>
