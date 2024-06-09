<template>
  <div class="wrapper">
    <h4 class="balance"> {{ count }} $</h4>
    <h1 class="war">wraning</h1>
    <span class="monet" @click="count ++">$</span>
    <h1 class="title">Mashka coin</h1>
    <h1 class="after-coin">After: <a href="https://t.me/notcoinchatuzbekistan">Umurbek@gmail.com</a> </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    }
  }
}
</script>

<style>

</style>
