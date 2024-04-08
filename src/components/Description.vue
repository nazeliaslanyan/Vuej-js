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
    <span>Description: {{ description }}</span>
  </div>
</template>