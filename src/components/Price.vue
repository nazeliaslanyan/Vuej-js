<script>
export default {
  props: {
    value: {
      type: String,
      required: true,
    },
  }
}
</script>



<template>
  <div>
    <span>Price: {{ price }}</span>
  </div>
</template>