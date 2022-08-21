<script>
import Product from "@/components/Product"

export default {
  components: {
    Product
  },
  data() {
    return {
      baseUrl: "http://fvt-market.com:1337",
      products: []
    }
  },
  mounted() {
    fetch( this.baseUrl + "/api/products?populate=photos")
      .then(res => res.json())
      .then(data => this.products = data.data)
      .catch(err => console.log(err.message))
  }
}
</script>

<template>
  <div class="container my-6">
    <p class="is-size-2 has-text-centered is-underlined mb-6">Products</p>

    <div class="columns px-6">
      <div class="column" v-for="product in products" :key="product.id">
        <div class="card">
          <div class="card-image">
            <figure class="image is-square">
              <img :src="baseUrl + product.attributes.photos.data[0].attributes.url">
            </figure>
          </div>
          <div class="card-content">
            <p class="title"><NuxtLink :to="'/products/' + product.id">{{ product.attributes.name }}</NuxtLink></p>
            <p class="subtitle">{{ product.attributes.resellPrice }}€</p>
          </div>
        </div>
      </div>

      <div class="column"></div>
      <div class="column"></div>
      <div class="column"></div>
    </div>
  </div>
</template>

<style scoped>

</style>
