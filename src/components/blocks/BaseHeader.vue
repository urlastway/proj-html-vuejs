<template>
  <header class="header">
    <div class="header__background">
      <HeaderMessage />
      <HeaderMenu />
      <HeaderInner />
      <HeaderButtom />
    </div>
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
  }
  .header__background{
    width: 100%;
    background-image: url(../../assets/img/header__inner__img/homepage-hero-background.jpg);
    background-repeat: no-repeat;
    position: relative;
    z-index: 0;
  }
  .header__background::before{
    width: 100%;
    height: 230px;
    content: '';
    background-color: rgba(0, 0, 0, 0.5);
    position: absolute;
    z-index: -1;
  }
</style>