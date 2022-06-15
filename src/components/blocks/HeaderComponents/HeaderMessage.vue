<template>
    <div class="header__message">
      <div class="container">
        <div class="header__message__content">
          <div class="header__message__content__left">
            <p>We heve a 95% Successful Pass Rate</p>
          </div>
          <div class="header__message__content__right">
            <i class="fa-solid fa-phone-flip"></i>
            <p>Give ua a call to book your tuition! 1-800-555-555</p>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderMessage',
}
</script>

<style lang="scss" scoped>

  .header__message{
      width: 100%;
      height: 60px;
      background-color: var(--color__design__AztecDarkMuted);
      display: flex;
      justify-content: center;    
    }
  .header__message__content{
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    &__right{
      display: flex;
      padding: 0 10px;;

      p{
        padding-left: 1rem;
      };

    };

  };

  p{
      color: var(--color__cut__AthensGray);
  };
  .fa-phone-flip{
    color: #fff;
  }
</style>