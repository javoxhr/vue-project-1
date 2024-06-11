<template>
  <div>
    <div class="cart">
        <div class="cart__wrapper">
            <a href="/" class="btn-back">Назад</a>
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
        }
    },
    methods: {
        getDetailProduct() {
            fetch('https://fakestoreapi.com/products' + this.$route.params.id)
            .then((res)=> res.json())
            .then((data)=> {
                this.detail = data
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