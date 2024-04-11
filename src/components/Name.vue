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
    <span>Name: {{ value }}</span>
  </div>
</template>