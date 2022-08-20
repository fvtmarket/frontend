<script>
import Navbar from "@/components/Navbar"

export default {
  components: {
    Navbar
  }
}
</script>

<template>
  <section class="hero is-halfheight">
    <div class="hero-body">
      <div class="container has-text-centered">
        <p class="is-size-1 my-4">Giorgio Store</p>
        <p class="is-size-6 my-4">Solo per veri uomini</p>
        <NuxtLink to="/" class="button my-4">Vai ai prodotti</NuxtLink>
      </div>
    </div>
    <div class="hero-foot">
      <Navbar />
    </div>
  </section>
</template>

<style scoped>
  .hero {
    background-color: #AA8788;
  }

  .button {
    color: #FFFFFF;
    background-color: #BEC1A6;
  }

  p {
    color: #FFFFFF;
  }
</style>
