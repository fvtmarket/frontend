<script>
export default {
  data() {
    return {
      isActive: false
    }
  }
}
</script>

<template>
  <div class="container">
    <div>
      <p class="is-size-4 has-text-centered has-text-weight-bold pt-4">FVT</p>
    </div>

    <hr>

    <nav class="navbar mb-4">
      <div class="navbar-brand">
        <a class="navbar-burger" data-target="collapse" @click="isActive = !isActive">
          <span></span>
          <span></span>
          <span></span>
        </a>
      </div>

      <div id="collapse" class="navbar-menu" :class="{'is-active': isActive}">
        <div class="navbar-start">
          <NuxtLink to="/" class="navbar-item">Featured</NuxtLink>
          <NuxtLink to="/" class="navbar-item">Categories</NuxtLink>
          <NuxtLink to="/" class="navbar-item">About Us</NuxtLink>
        </div>

        <div class="navbar-end">
          <NuxtLink to="/" class="navbar-item"><i class="fa-solid fa-magnifying-glass"></i></NuxtLink>
          <NuxtLink to="/" class="navbar-item"><i class="fa-solid fa-user"></i></NuxtLink>
          <NuxtLink to="/" class="navbar-item"><i class="fa-solid fa-basket-shopping"></i></NuxtLink>
        </div>
      </div>
    </nav>
  </div>
</template>

<style scoped>

</style>
