<script>
import Navbar from "@/components/Navbar"
import Footer from "@/components/Footer"

export default {
  components: {
    Navbar,
    Footer
  },
  data() {
    return {
      baseUrl: "http://fvt-market.com:1337",
      product: null,
      loaded: false
    }
  },
  mounted() {
    fetch( this.baseUrl + "/api/products/" + this.$route.params.id + "/?populate=photos")
      .then(res => res.json())
      .then(data => {
        this.product = data.data
        this.loaded = true
      })
      .catch(err => console.log(err.message))
  }
}
</script>

<template>
  <div>
    <Navbar />

    <div class="container my-6">
      <div class="box">
        <div class="columns">
          <div class="column">
            <figure class="image is-square is-rounded">
              <img :src="baseUrl + product.attributes.photos.data[0].attributes.url" v-if="loaded">
            </figure>
          </div>
          <div class="column">

          </div>
        </div>
      </div>
    </div>

    <Footer />
  </div>
</template>
