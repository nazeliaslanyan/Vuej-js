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
    
    <button @click="checkEmail()">Input Email</button>

    <h1></h1> 
    <h4 v-if="emailIsValid">The email is valid</h4>
    <h4 v-else>The email is invalid</h4>

    
    <button @click="resetEmail()">Reset</button>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
