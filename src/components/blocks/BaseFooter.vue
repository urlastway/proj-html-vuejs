<template>
  <footer class="footer">
    <div class="footer__top">
      <div class="container">
        <div class="footer__top__content">
          <div class="footer__card">
            <img src="../../assets/img/logo/avada-drivers-logo-1x.png" class="footer__logo">
            <p class="logo__text">Avada Driving School is the right choice for Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis similique mollitia</p>
          </div>
          <div class="footer__card">
            <h1 class="footer__name__section">Contacts Details</h1>
            <div class="footer__links" v-for="info in informations" :key="info">
              <i class="fa-solid fa-house-${info.icon} fa-xl"></i>
              <a href="#"><p>{{info.contact}}</p></a>
            </div>
          </div>
          <div class="footer__card">
            <h1 class="footer__name__section">Courses</h1>
            <div class="footer__links" v-for="course in courses" :key="course">
              <i class="fa-solid fa-circle-arrow-right fa-xl"></i>
              <a href="#"><p>{{course.name}}</p></a>
            </div>
          </div>
          <div class="footer__card">
            <img src="../../assets/img/footer/footer-ad-grid.png" class="footer__logo">
            <button class="footer__button"><p class="footer__button__text">Book Now</p></button>
          </div>
        </div>
      </div>
    </div>
    <div class="footer__bottom">

    </div>
  </footer>
</template>

<script>
export default {
    name: 'BaseFooter',
    data(){
      return {
        informations: [
          {
            icon: 'user',
            contact: '12345 North Main Street New Youk, NY 555555'
          },
          {
            icon: 'phone-flip"',
            contact: '1.800.555.6789'
          },
          {
            icon: 'envelope',
            contact: 'info@your-domain.com'
          },
          {
            icon: 'link',
            contact: 'Theme-Fusion.com'
          },
        ],
        
        Courses: [
          {
            name: 'Pass Plus',
          },
          {
            name: 'Intensive course',
          },
          {
            name: 'Automatic',
          },
          {
            name: 'Instructor Training',
          },
        ]
      }
    },
}
</script>

<style lang="scss" scoped>

.footer{
  width: 100%;
}
.footer__top{
  width: 100%;
  height: 500px;
  background-image: url(../../assets/img/footer/footer-background-color.jpg);
  display: flex;
  justify-content: center;
  
}
.footer__bottom{
  width: 100%;
  height: 145px;
  background-color:  #1c1d1e;
}
.footer__top__content{
  width: 100%;
  display: flex;
}
.footer__card{
  width: calc(100% / 4);
  display: flex;
  flex-direction: column;
  padding-top: 100px;
  color: var(--color__footer__text);

  img{
    width: 280px;
  }
  p{
    padding-top: 20px;
    line-height: 2;
  }
  .footer__name__section{
    color: var(--color__cube__wite);
    font-size: 25px;
    font-weight: 500;
    text-transform: uppercase;
    margin-left: 30px;
    margin-bottom: 20px;
  }
  .footer__links{
    display: flex;
    align-items: center;
    justify-content: flex-start;
    color: var(--color__footer__text);
    margin-left: 30px;
    margin-top: 10px;

    a{
      text-decoration: none;
      color: var(--color__footer__text);
      
      p{
        padding-top: 0;
        margin-left: 20px;
      }
    }
  }
/*BUTTONS*/
.footer__button {
    margin-top: 20px;
    outline: none;
    cursor: pointer;
    text-align: center;
    text-decoration: none;
    color: #fff;
    padding: 15px ;
    background: var(--color__cube__BayLeaf);
    border: none;
    border-radius: 30px;
    border: solid 2px var(--color__cube__BayLeaf);

    .footer__button__text{
        padding: 0;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 15px;
    }

    }
.footer__button:hover{
        background-color: var(--color__cube__wite);
        transition: 0.3s;
        border: solid 2px var(--color__cube__BayLeaf);
        color: var(--color__cube__BayLeaf)
    }
}
</style>