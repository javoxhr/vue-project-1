<template>
    <a href="/" class="btn-back">Назад</a>
    <h3 class="product-catigor">{{ detail.category }}</h3>
    <div
      class="loader"
      :style="{ display: loading == true ? 'block' : 'none' }"
    >
      <div class="load-wrap">
        <span class="round"></span>
        <span class="round"></span>
        <span class="round"></span>
        <span class="round"></span>
        <span class="round"></span>
        <span class="round"></span>
      </div>
    </div>
  <div class="card-main-wrapper">
    <div class="card">
        <div class="container">
            <div class="card__wrapper">
            <div class="card__img">
                    <img :src="detail.image" :alt="detail.title">
            </div>
            <div class="card__text-wrapper">
                <h1 class="card__title">{{ detail.title }}</h1>
                <div class="card__price-wrapper">
                    <h2 class="card__price">{{ detail.price }}$</h2>
                    <h2 class="card-price-sale">{{ Math.round(detail.price * 1.5) }}$</h2>
                </div>

                <div class="card__rating">
                    <h2>{{ detail?.rating?.rate }}</h2>
                    <img src="../assets/images/star.svg" alt="">
                    <h2>{{ detail?.rating?.count }} отзывов</h2>
                </div>

                <p class="card__desc">{{ detail.description }}</p>

                <button class="add-to-cart">В корзину</button>
            </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            baseUrl: 'https://fakestoreapi.com',
            detail: {},
            mainImgIndex: 0,
            loading: true,
        }
    },
    methods: {
        getDetailProduct() {
            fetch('https://fakestoreapi.com/products/' + this.$route.params.id)
            .then((res)=> res.json())
            .then((data)=> {
                this.detail = data
                this.loading = false
            })
        }
    },
    mounted() {
        this.getDetailProduct()
    }
}
</script>

<style>

</style>