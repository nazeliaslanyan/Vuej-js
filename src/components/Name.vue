<script>
export default {
  props: {
    value: {
      type: String,
      required: true,
    }
  }
};
</script>



<template>
  <div>
    <span>Name: {{ name }}</span>
  </div>
</template>