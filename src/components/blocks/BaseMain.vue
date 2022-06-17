<template>
  <main>
    <div class="main__first__style">
      <MainFirst />

    </div>
  </main>
</template>

<script>
import MainFirst from './MainComponents/MainFirst';
export default {
    name: 'BaseMain',
    components: {
    MainFirst,
}
}
</script>

<style lang="scss" scoped>
.main__first__style{
  width: 100%;
  height: 900px;
  background-image: url(../../assets/img/learning__drive/promise-background.jpg);
  background-size: cover;
  position: absolute;
  z-index: 0;
}
.main__first__style::before{
  width: 100%;
  height: 300px;
  content: '';
  position: absolute;
  background-image: url(../../assets/img/learning__drive/horizontal-cta-background.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  z-index: -1;
}
.main__first__style::after{
  margin-top: 150px;
  width: 100%;
  content: '';
  position: absolute;
  background-color: #fff;
  z-index: -1;
}
</style>