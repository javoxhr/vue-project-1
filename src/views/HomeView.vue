<template>
  <div>
    <header>
      <div class="container">
        <div class="header-wrapper">
          <div class="header-top">
            <div class="header-top__list">
              <span class="header-top__list-li">Покупателям <img src="../assets/images/arrow-bottom.png" alt=""></span>

              <span class="header-top__list-li">Покупателям <img src="../assets/images/arrow-bottom.png"  alt=""></span>

               <span class="header-top__list-li">Покупателям <img src="../assets/images/arrow-bottom.png" alt=""></span>
            </div>

            <div class="lang">
              <div class="lang__wrapper">
                <img class="lang__img" src="../assets/images/Flag Ru.png" alt="">
                <h1 class="lang__text">Русский</h1>
                <span class="lang__valyut">₽ <img src="../assets/images/arrow-bottom.png" alt=""> </span>
              </div>
            </div>
          </div>

          <div class="header-bottom">
            <div class="header-bottom-wrapper">
              <button class="header-bottom__menu"><img src="../assets/images/menu.svg" alt=""></button>
              <router-link><img class="logo" src="../assets/images/logo.svg" alt=""></router-link>

              <div class="search">
                <input class="header-bottom__input" type="text">
                <button class="header-bottom__search-btn">Везде <img src="../assets/images/arrow-bottom.png" alt=""></button>
                <button class="search__logo"><img src="../assets/images/header-search.png" alt=""></button>
              </div>

              <div class="login">
                <div class="login-wrap">
                  <div class="login__item">
                    <img src="../assets/images/user.png" alt="">
                    <h1>Войти</h1>
                  </div>

                  <div class="login__item">
                    <img src="../assets/images/like.png" alt="">
                    <h1>Избранное</h1>
                  </div>

                  <div class="login__item">
                    <img src="../assets/images/cart.png" alt="">
                    <h1>Корзина</h1>
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
          <a href="#" class="main-hero-img"><img src="../assets/images/hero-img.jpg" alt=""></a>
          <div class="two-product">
            <a href="#"><img src="../assets/images/two-products-one.jpg" alt=""></a>
            <a href="#"><img src="../assets/images/two-products-two.jpg" alt=""></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
