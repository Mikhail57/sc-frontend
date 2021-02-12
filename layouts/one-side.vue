<template>
  <div>
    <section class="hero main-content columns is-fullheight left-image">
      <div class="hero-body columns">
        <div class="column is-4 is-offset-half">
          <nuxt />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.left-image {
  background: url('~assets/left_bg.png') no-repeat left;
  background-size: 50%;
}
</style>
