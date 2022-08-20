<script>
import Product from "@/components/Product"

export default {
  components: {
    Product
  }
}
</script>

<template>
  <div class="container m-6">
    <p class="is-size-2 has-text-centered is-underlined mb-6">Featured</p>

    <div class="columns">
      <div class="column">
        <Product />
      </div>
      <div class="column">
        <Product />
      </div>
      <div class="column">
        <Product />
      </div>
      <div class="column">
        <Product />
      </div>
    </div>
  </div>
</template>
