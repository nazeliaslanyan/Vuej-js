<script>
export default {
  data: function() {
    return {
      email: '', 
      emailIsValid: false 
    };
  },
  methods: {
    
    checkEmail() {
      const inputEmail = prompt("Please enter your email:");
      if (inputEmail !== null) {
        this.email = inputEmail.trim();
        this.emailIsValid = this.validateEmail(this.email);
      }
    },
    
    validateEmail(email) {
      const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return regex.test(email);
    },
    
    resetEmail() {
      this.email = '';
      this.emailIsValid = false;
    }
  }
}
</script>

<template>
  <div>
    
    <button @click="checkEmail">Input Email</button>

    <h1 :style="{ borderColor: emailIsValid ? 'green' : 'red' }">{{ email }}</h1>
    <h4 v-if="emailIsValid">The email is valid</h4>
    <h4 v-else>The email is invalid</h4>

    
    <button @click="resetEmail">Reset</button>
  </div>
</template>


<style scoped>
h1 {
  border: 2px solid;
  padding: 5px;
}
</style>
