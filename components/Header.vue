<template>
  <h1><slot></slot></h1>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
h1 {
  font-weight: 700;
  font-size: 35px;
  color: black;
}
</style>
