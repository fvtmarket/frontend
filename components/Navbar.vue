<script>
export default {
  data() {
    return {
      isActive: true
    }
  }
}
</script>

<template>
  <div class="tabs is-centered pt-2">
    <ul>
      <li><NuxtLink to="/">Home</NuxtLink></li>
      <li><NuxtLink to="/">About</NuxtLink></li>
      <li><NuxtLink to="/">Cart</NuxtLink></li>
    </ul>
  </div>
</template>

<style scoped>
  .tabs {
    background-color: #181416;
  }

  a {
    color: #FFFFFF;
  }
</style>
