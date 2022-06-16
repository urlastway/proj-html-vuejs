<template>
  <div class="main__first">
    <div class="container">
        <div class="main__content">
            <div class="main__content__left">
                <h1>Start Learning to Drive Today</h1>
                <h3>Give us a call to shedule your first driving lesson</h3>
            </div>
            <div class="main__content__right">
                <i class="fa-solid fa-phone-flip"></i>
                <p class="number">1-800-555-555</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'MainFirst',
}
</script>

<style lang="scss" scoped>
.main__first{
    width: 100%;
    display: flex;
    justify-content: center;
}
.main__content{
    height: 270px;
    display: flex;
    justify-content: space-between;
    color: var(--color__cube__wite);
    align-items: center;

    &__right{
        display: flex;
        align-items: center;
        
        .number{
        font-size: 30px;
    }
    }

}
.fa-phone-flip{
    font-size: 30px;
    margin-right: 20px;
}
</style>