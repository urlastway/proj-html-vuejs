<template>
  <header class="header">
      <HeaderMessage />
      <HeaderMenu />
      <HeaderInner />
      <HeaderButtom />
  </header>
</template>


<script>

import HeaderMessage from './HeaderComponents/HeaderMessage';
import HeaderMenu from './HeaderComponents/HeaderMenu';
import HeaderInner from './HeaderComponents/HeaderInner';
import HeaderButtom from './HeaderComponents/HeaderButtom';



export default {
    name: 'BaseHeader',
    components: {
    HeaderMessage,
    HeaderMenu,
    HeaderInner,
    HeaderButtom,
}
}
</script>

<style lang="scss" scoped>
  .header{
    width: 100%;
    height: 100vh;
    background-image: url(../../assets/img/header__inner__img/homepage-hero-background.jpg);
    position: relative;
    z-index: 0;
  }
  .header::before{
    width: 100%;
    height: 230px;
    content: '';
    background-color: rgba(0, 0, 0, 0.5);
    position: absolute;
    z-index: -1;
  }
  .header::after{
    width: 100%;
    height: auto;
    background-color: #fff;
    content: '';
    position: absolute;
    opacity: 0.5;

  }
</style>