<template>
  <div>
    <loader :style="{ display: loading == true ? 'block' : 'none' }"></loader>
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
    <header>
      <div class="container">
        <div class="header-wrapper">
          <div class="header-top">
            <div class="header-top__list">
              <span class="header-top__list-li"
                >Покупателям
                <img src="../assets/images/arrow-bottom.png" alt=""
              /></span>

              <span class="header-top__list-li"
                >Покупателям
                <img src="../assets/images/arrow-bottom.png" alt=""
              /></span>

              <span class="header-top__list-li"
                >Покупателям
                <img src="../assets/images/arrow-bottom.png" alt=""
              /></span>
            </div>

            <div class="lang">
              <div class="lang__wrapper">
                <img
                  class="lang__img"
                  src="../assets/images/Flag Ru.png"
                  alt=""
                />
                <h1 class="lang__text">Русский</h1>
                <span class="lang__valyut"
                  >₽ <img src="../assets/images/arrow-bottom.png" alt="" />
                </span>
              </div>
            </div>
          </div>

          <div class="header-bottom">
            <div class="header-bottom-wrapper">
              <button
                class="header-bottom__menu"
                @click="
                  showFunc(),
                    (styleTwoCard = show ? 'none' : 'flex'),
                    (styleHeight = show ? '400' : '365')
                "
              >
                <img src="../assets/images/menu.svg" alt="" />
              </button>
              <a href="#"
                ><img class="logo" src="../assets/images/logo.svg" alt=""
              /></a>

              <div class="search">
                <div class="input-search-wrap">
                  <input class="header-bottom__input" type="text" />
                </div>
                <button class="header-bottom__search-btn">
                  Везде <img src="../assets/images/arrow-bottom.png" alt="" />
                </button>
                <button class="search__logo">
                  <img src="../assets/images/header-search.png" alt="" />
                </button>
              </div>

              <div class="login">
                <div class="login-wrap">
                  <div class="login__item">
                    <img src="../assets/images/user.png" alt="" />
                    <h1>Войти</h1>
                  </div>

                  <div class="login__item">
                    <img src="../assets/images/like.png" alt="" />
                    <h1>Избранное</h1>
                  </div>

                  <div class="login__item">
                    <button class="open-cart" @click="right = 0">
                      <img src="../assets/images/cart.png" alt="" />
                      <h1>Корзина</h1>
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </header>

    <div class="hero">
      <div class="container">
        <div class="hero-wrapper">
          <div
            class="populyar-catigor"
            :style="{ display: show ? 'block' : 'none' }"
          >
            <div class="popular-catigor__wrapper">
              <span class="populyar-catigor__item-title"
                ><img src="../assets/images/toch-3-menu.png" alt="" />Популярные
                категории</span
              >

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Компьютеры и оргтехника
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Электроника
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Бытовая техника
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Одежда для женщин
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Одежда для мужчин
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Все для детей
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Автотовары
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Красота и здоровье
              </span>

              <span class="populyar-catigor__item">
                <img src="../assets/images/catigor-item-1.svg" alt="" />
                Спорт и развлечения
              </span>
            </div>
          </div>
          <a href="#" class="main-hero-img"
            ><img
              src="../assets/images/hero-img.jpg"
              alt=""
              :style="{ height: styleHeight + 'px' }"
          /></a>
          <div class="two-product" :style="{ display: styleTwoCard }">
            <a href="#"
              ><img src="../assets/images/two-products-one.jpg" alt=""
            /></a>
            <a href="#"
              ><img src="../assets/images/two-products-two.jpg" alt=""
            /></a>
          </div>
        </div>
      </div>
    </div>

    <div class="buy-product">
      <div class="container">
        <div class="buy-product__wrapper">
          <h1 class="buy-product__title">
            Успей купить <span v-if="loading">loading</span>
          </h1>
          <div class="buy-product-cards-wrapper">
            <AboutProductCard
              v-for="item in products"
              :key="item"
              :product="item"
            />
          </div>
          <div class="all-products-btn-wrap">
            <div class="all-btn">
              <button class="all-products-btn">Все товары</button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="cart" :style="{'right': right + '%'}">
      <div class="cart__wrapeer">
        <div class="cart__header">
          <h1>My order</h1>
          <button class="cart-close" @click="right = -100">
            <img src="../assets/images/cart.png" alt="">
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import AboutProductCard from "../components/AboutProductCard.vue";
// import Loader from "../components/Loader.vue";

export default {
  components: { AboutProductCard },
  // components: {Loader},
  data() {
    return {
      baseUrl: "https://api.escuelajs.co/api/v1",
      displayStayle: "none",
      styleTwoCard: "flex",
      styleHeight: "365",
      show: false,
      products: [],
      loading: true,
      right: -100,
      index: 0,
    };
  },
  methods: {
    showFunc() {
      this.show = !this.show;
    },
    getData() {
      this.loading = true;
      fetch("https://fakestoreapi.com/products")
        .then((res) => res.json())
        .then((data) => {
          this.products = data;
          console.log(data);
          this.loading = false;
        });
    },
  },
  mounted() {
    this.getData();
  },
};
</script>

<style lang="scss" scoped>
</style>