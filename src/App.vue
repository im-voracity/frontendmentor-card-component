<template>
  <ProductPreview></ProductPreview>
</template>

<script>
import ProductPreview from "@/components/ProductPreview";

export default {
  name: 'App',
  components: {
    ProductPreview
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
  }

body {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: hsla(28, 38%, 92%, 1);
}
</style>
