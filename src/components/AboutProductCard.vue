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
                </div>
            </div>
        </div>
    </div>
</template>

<script>
 export default {
    props: ['product']
 }
</script>

<style lang="scss" scoped>
  
</style>