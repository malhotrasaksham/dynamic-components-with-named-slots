<template>
  <div>
    <slot></slot>
    <div class="red">
      <slot name="colored"></slot>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.red {
  color: red;
}
</style>
