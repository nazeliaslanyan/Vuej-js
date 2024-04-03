
  <script>
  import Name from './components/Name.vue';
  import Price from './components/Price.vue';
  import Description from './components/Product.vue';
  
  export default {
    components: {
      Name,
      Price,
      Description
    },
    props: {
      fruit: Object
    }
  };
  </script>
  
  
  <template>
    <div class="product">
      <Name :value="fruit.name" />
      <Price :value="fruit.price" />
      <Description :value="fruit.description" />
    </div>
  </template>