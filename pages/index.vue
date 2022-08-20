<script>
import Navbar from "@/components/Navbar"
import Hero from "@/components/Hero"
import Products from "@/components/Products"
import Footer from "@/components/Footer"

export default {
  components: {
    Navbar,
    Hero,
    Products
  }
}
</script>

<template>
  <div>
    <Navbar />
    <Hero />
    <Products />
    <Footer />
  </div>
</template>

<style>
  *:hover {
    outline: 1px blue solid;
  }

  * {
    font-family: 'Times New Roman', Times, serif;
  }
</style>
