<script>
export default {
  data: function() {
    return {
        exchange:{},
      
    };
  },
  methods: {
    
   
    },
    
   
}
</script>

<template>
<div>
    <input 
      type="number"
      v-model="enterAmount"
      @input="convertCurrency"
    >
    <input 
      type="number"
      v-model="convertAmount"
      @input="handleInputChange"
    >
    <button @click="toggleMode">Toggle Mode</button>
  </div>
  
</template>


<style scoped>

</style>
