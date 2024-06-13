<template>
    <div class="product-card">
        <div class="about-product">
            <div class="product-wrapper">
                <img :src="product.image" :alt="product.title" class="product-img">
                <div class="product-text-wrapper">
                    <div class="price-wrap">
                        <h3 class="product-price">{{ product.price }} $</h3>
                        <h3 class="before-price">{{ Math.round(product.price * 1.5)}} $</h3>
                    </div>
                    <div class="reting">
                        <span>{{product.rating.rate}} <img class="start-img" src="../assets/images/star.svg" alt="">{{ product.rating.count }} отзывов</span>
                    </div>
                    <router-link :to="`/product/${product.id}`">
                        <p class="product-title">{{ product.title }}</p>
                    </router-link>
                    <div class="about-product__cart-btn">
                        <button>В корзину</button>
                    </div>
                    <span class="sale">-25%</span>
                    <span class="like" :class="{'like-after-click': show == true}" @click="likeFunc()">
                        <span class="like-anim">1</span>
                        <!DOCTYPE svg  PUBLIC '-//W3C//DTD SVG 1.1//EN'  'http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd'><svg enable-background="new 0 0 50 50" height="50px" id="Layer_1" version="1.1" viewBox="0 0 50 50" width="30px" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><rect fill="none" height="50" width="50"/><path d="M35,8  c-4.176,0-7.851,2.136-10,5.373C22.851,10.136,19.176,8,15,8C8.373,8,3,13.373,3,20c0,14,16,21,22,26c6-5,22-12,22-26  C47,13.373,41.627,8,35,8z" fill="transparet" stroke="transparet" stroke-linecap="round" stroke-miterlimit="10" stroke-width="2"/></svg>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
 export default {
    props: ['product'],
    data() {
        return {
            colorLike: 'red',
            show: false,
        }
    },
    methods: {
        likeFunc() {
            this.show = !this.show
        }
    }
 }
</script>

<style lang="scss" scoped>
  
</style>