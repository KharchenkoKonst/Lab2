<template>
  <section class="content">
    <Header></Header>
    <main class="container">
      <div class="product-title">
        <h1>{{ product.title }}</h1>
      </div>

      <div class="info">
        <div class="product-image">
          <img :src=product.image class="book-img-cover" alt="">
        </div>

        <div class="product-description">
          <div id="age_dopusk" title="Рекомендуемый возраст">{{ product.age }}+</div>
          <div class="authors">Год: {{ product.year }}</div>
          <div class="genre">Жанр: {{ product.genre }}</div>

          <div class="buying">
            <div class="buying-price">
              <div class="buying-rate-text">Рейтинг: {{ product.rate }}</div>
            </div>
            <a href="#" class="btn"><span class="text">Добавить <span>в корзину</span></span></a>

          </div>
        </div>
        <hr/>


        <div class="product-about">
          <h4>Аннотация к фильму {{ product.author }}: "{{ product.title }}"</h4>
          <div class="annotation">
            <p>
              {{ product.description }}
            </p>
          </div>
        </div>
      </div>

    </main>
    <Footer></Footer>
  </section>
</template>

<script>
import Footer from "./Footer";
import Header from "./Header";
import Product from "./Product";

export default {
  name: "ContentPage",
  components: {
    Footer,
    Header,
    Product
  },
  data() {
    return {
      id: null,
      product: null
    }
  },
  created() {
    this.id = this.$route.params.id
    this.product = this.$route.params.product
  }
}
</script>

<style scoped src="../assets/styles/content-style.css">

</style>