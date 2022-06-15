<template>
  <div id="app">
    <BaseHeader />
    <BaseMain />
    <BaseFooter />
  </div>
</template>

<script>
import BaseHeader from './components/blocks/BaseHeader.vue';
import BaseFooter from './components/blocks/BaseFooter.vue';
import BaseMain from './components/blocks/BaseMain.vue';


export default {
    components: {
    BaseHeader,
    BaseFooter,
    BaseMain
}
}
</script>

<style lang="scss">

@import './assets/Style/global.scss'; /*Global*/

</style>
