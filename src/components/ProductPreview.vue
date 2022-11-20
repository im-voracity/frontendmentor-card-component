<template>
  <div class="content">
    <picture class="item-picture">
      <source
      :srcset="require('../assets/image-product-mobile.jpg')"
      media="(max-width: 650px)"
      >
      <img :src="require('../assets/image-product-desktop.jpg')" alt="A Perfume Chanel-branded with some leaves next to it">
    </picture>
    <div class="data">
      <h2 class="category">Perfume</h2>
      <h1 class="product-name">Gabrielle Essence Eau De Parfum</h1>
      <p class="product-description">A floral, solar and voluptuous interpretation composed by Olivier Polge,
        Perfumer-Creator for the House of
        CHANEL.</p>
      <div class="pricing">
        <p class="current-price">$149.99</p>
        <p class="old-price">$169.99</p>
      </div>
      <MainButton name="Add To Cart" href="#"></MainButton>
    </div>
  </div>
</template>

<script>
import MainButton from "@/components/MainButton";

export default {
  name: "ProductPreview",
  components: {MainButton},
};
</script>

<style scoped>
.content {
  width: 600px;
  height: 450px;
  background-color: white;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  border-radius: 10px;
}

.item-picture {
  max-width: 50%;
  height: 100%;
}

source, img {
  width: 100%;
  height: 100%;
}

.data {
  width: 50%;
  height: 100%;
  padding: 32px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.category {
  margin-bottom: 20px;
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  font-size: 12px;
  color: hsla(228, 12%, 48%, 1);
  text-transform: uppercase;
  letter-spacing: 5px;
  line-height: 15px;
}

.product-name {
  margin-bottom: 24px;
  font-family: 'Fraunces', serif;
  font-weight: 700;
  font-size: 32px;
  line-height: 32px;
  color: hsla(212, 21%, 14%, 1);
}

.product-description {
  margin-bottom: 29px;
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  font-size: 14px;
  line-height: 23px;
  color: hsla(228, 12%, 48%, 1);
}

.pricing {
  margin-bottom: 30px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 194px;
}

.current-price {
  font-family: 'Fraunces', serif;
  font-weight: 700;
  font-size: 32px;
  line-height: 32px;
  color: hsla(157, 36%, 37%, 1);
}

.old-price {
  text-decoration: line-through;
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  font-size: 13px;
  line-height: 23px;
  color: hsla(228, 12%, 48%, 1);
}

@media screen and (max-width: 650px) {
  .content {
    width: 343px;
    height: 611px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .item-picture {
    width: 100%;
    height: 240px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  picture img {
    width: 343px;
    height: 240px;
  }

  .data {
    width: 100%;
    max-height: 371px;
    padding: 24px;
  }

  .category {
    margin-bottom: 12px;
  }

  .product-name {
    margin-bottom: 16px;
  }

  .product-description {
    margin-bottom: 24px;
  }

  .pricing {
    margin-bottom: 20px;
  }

} main-button {
  min-height: 48px;
  }

</style>