<template>
  <div class="header__buttom">
    <div class="container">
      <div class="header__buttom__content">
          <div class="header__buttom__left">
              <h1 class="title">Get Behind The Wheel</h1>
              <h2 class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus explicabo alias numquam, quaerat adipisicing elit. Autem impedit sunt</h2>
              <p class="header__buttom__text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem impedit sunt a quis corrupti quae, quod eaque libero cupiditate, tempora explicabo accusantium et, earum aut omnis quos alias ipsam nam! Lorem ipsum dolor sit amet consectetur adipisicing elit. Est beatae perspiciatis sunt et harum, recusandae animi ex, laborum laudantium, hic facere cum nemo aliquid? Dolor facilis eos amet perspiciatis aliquam.</p>
          </div>
          <div clss="header__buttom__right">
              <div class="prenotation">

              </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'HeaderButtom',
}
</script>

<style lang="scss" scoped>

.header__buttom{
  width: 100%;
  height: 700px;
  display: flex;
  justify-content: center;

  &__content{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: var(--color__cube__tundora);

  }
  &__left{
    width: calc(100% / 2);
  }
  &right{
    width: calc(100% / 2);
  }
}

.prenotation{
  width: 600px;
  height: 600px;
  background-color: #fff;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  }
.title{
  font-size: 2.5rem;
  padding-bottom: 1rem;
  }
.subtitle{
  padding-bottom: 1rem;
  font-size: 1.3rem;
  font-weight: 500;
  line-height: 2;
  }
.header__buttom__text{
  font-weight: 300;
  line-height: 2;
  }
</style>