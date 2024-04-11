<script>
import Name from './Name.vue';
import Price from './Price.vue';
import Description from './Description.vue';

export default {
  components: {
    Name,
    Price,
    Description
  },
  props: {
    fruit: {
      type: Object,
      required: true
    }
  },
  methods: {
    onButtonChlick() {
      this.$emit('currencyChange')
    }
  }
};
</script>


<template>
  <div class="product">
    <Name :value="fruit.name" />
    <Price :value="fruit.price" />
    <Description :value="fruit.description" />
    <button @click="onButtonChlick"> Change the currency</button>
  </div>
</template>