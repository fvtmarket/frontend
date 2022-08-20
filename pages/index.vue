<script>
import Hero from "@/components/Hero"
import Products from "@/components/Products"

export default {
  components: {
    Hero,
    Products
  }
}
</script>

<template>
  <div>
    <Hero />
    <Products />
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
