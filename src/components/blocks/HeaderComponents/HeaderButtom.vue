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
                <h1 class="title__right">First Leson Free!</h1>
                <p class="subtitle__right">When you make a block booking with us your first lesson is included free</p>
                <form action="" v-for="(data, index) in datas" :key="index">
                  <input type="text" :placeholder="data.name" v-modul="data.user__information"/>
                </form>
                <button class="header__bottom__button"><p>Request a callback</p></button>
              </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'HeaderButtom',
    data(){
      return {
        datas: [
          {
            name: "Your Name*",
            user__information: ""
          },
          {
            name: "Email",
            user__information: ""
          },
          {
            name: "Telephone",
            user__information: ""
          },
          {
            name: "Location",
            user__information: ""
          },
        ]
      }
    }
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
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 50px;
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
.title__right{
  color: var(--color__cube__BayLeaf);
  font-weight: 500;
  margin-bottom: 20px;
}
.subtitle__right{
  text-align: center;
  line-height: 2;
  margin-bottom: 20px;
}
form {
  display: flex;
  flex-direction: column;
  width: 100%;
  
  input {
    height: 45px;
    border: solid 1px var(--color__cut__gumbo);
    border-radius: 5px;
    margin: 10px 0;
    background-color: rgb(233, 233, 233);
    font-size: 18px;
    font-weight: 300;
    padding: 10px;
  }
  input:hover{
    border: solid 1px var(--color__cut__CapeCod);
  }
}

/*--- Button ---*/
.header__bottom__button {
        margin-top: 20px;
        cursor: pointer;
        text-align: center;
        text-decoration: none;
        color: #fff;
        padding: 15px 20px;
        background: var(--color__cube__BayLeaf);
        border: none;
        border-radius: 20px;

        p{
            text-transform: uppercase;
            font-weight: 700;
            font-size: 15px;
        }

    }
.header__bottom__button:hover{
        background: var(--color__cut__BayLeaf);
        transition: 0.3s;
    }
</style>