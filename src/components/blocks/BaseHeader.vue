<template>
  <header class="header">
    <HeaderMessage />
    <HeaderMenu />
  </header>
</template>


<script>

import HeaderMessage from './HeaderComponents/HeaderMessage'
import HeaderMenu from './HeaderComponents/HeaderMenu'

export default {
    name: 'BaseHeader',
    components: {
    HeaderMessage,
    HeaderMenu,
}
}
</script>

<style lang="scss" scoped>
  .header{
    width: 100%;
    height: auto;
}
</style>