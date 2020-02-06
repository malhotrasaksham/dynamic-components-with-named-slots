<template>
  <div>
    <slot></slot>
    <div class="green">
      <slot name="colored"></slot>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.green {
  color: green;
}
</style>
