<template>
    <div clas="main">
        <div class="main__second">
            <div class="container">
                <div class="main__second__content">
                    <!--Instructors-->
                    <!--Instructors Prev--> 

                    <div class="main__second__content__top__instructors">
                        <div class="main__second__content__top__instructors__left">
                            <h1>Your Instructors</h1>
                            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et ipsum beatae sapiente nemo iure eos excepturi, quis consequuntur in animi nihil vel tempora ipsa enim dolore natus quaerat ducimus fuga.</p>
                        </div>
                        <div class="main__second__content__top__instructors__right">
                            <button class="main__top__button"><p class="main__top__button__text">More about us</p></button>
                        </div>
                    </div>
                    <!--/Instructors Prev-->

                    <!-- Instructors Cards-->

                    <div class="main__second__content__bottom__instructors">
                        <div class="main__second__content__bottom__instructors__cards" v-for="(instructor, index) in instructors" :key="index">
                            <img :src="instructor.image">
                            <h1 div class="instructor__name">{{instructor.name}}</h1>
                            <div class="instructors__icons">
                                <i class="fa-brands fa-facebook-f"></i>
                                <i class="fa-brands fa-twitter"></i>
                                <i class="fa-brands fa-instagram"></i>
                            </div>
                            <p>{{instructor.text}}</p>
                        </div>
                    </div>
                    <!-- /Instructors Cards-->
                    <!-- /Instructors--> 
                </div>
            </div>
        </div>
        <div class="main__third">
            <div class="container">
                <div class="testimonials">
                    <div class="testimonials___container">
                        <h1>Testimonials</h1>
                        <p class="comments">Here's what our happy drivers had to say about our services:</p>
                        <img src="../../../assets/img/testimonials/testimonial-grant.png">
                        <p class="testimonials__coments">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora</p>
                        <p class="testimonials__name">Sophia Jones</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'BaseSecond',
    data(){
        return{
            instructors: [
                {
                    name: 'Mike Hart',
                    image: require('../../../assets/img/instructors/instructor-mikehart.jpg'),
                    text: 'Lorem ipsum dolor sit amet dolor sit, lorem ipsum dolor sit',
                },
                {
                    name: 'John Smith',
                    image: require('../../../assets/img/instructors/instructor-johnsmith.jpg'),
                    text: 'Lorem ipsum dolor sit amet dolor sit, lorem ipsum dolor sit',
                },
                {
                    name: 'Angela Hart',
                    image: require('../../../assets/img/instructors/instructor-angelahart.jpg'),
                    text: 'Lorem ipsum dolor sit amet dolor sit, lorem ipsum dolor sit',
                },
            ],
            testimonials: [
                {
                    name: 'Sophia Jones',
                    img: require('../../../assets/img/testimonials/testimonial-sophia.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora',
                    current: true,
                },
                {
                    name: 'Harold Poping',
                    img: require('../../../assets/img/testimonials/testimonial-harold.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora',
                    current: false,
                },
                {
                    name: 'Kate Dash',
                    img: require('../../../assets/img/testimonials/testimonial-kate.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora',
                    current: false,
                },
                {
                    name: 'Kelly Kiely',
                    img: require('../../../assets/img/testimonials/testimonial-kelly.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora',
                    current: false,
                },
                {
                    name: 'Grant Hot',
                    img: require('../../../assets/img/testimonials/testimonial-grant.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora',
                    current: false,
                },
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.main__second{
    width: 100%;
    display: flex;
    justify-content: center;
    height: 600px;
    background-color: #fff;
}
.main__third{
    width: 100%;
    display: flex;
    justify-content: center;
    background-image: url(../../../assets/img/testimonials/testimonial-background.jpg);
    background-size: cover;
}
.main__second__content{
    display: flex;
    flex-direction: column;
    color: var(--color__cube__tundora);

    &__top__instructors{
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: center;

        &__left{
            width: calc(100% / 2 + 200px);
            display: flex;
            flex-direction: column;

            h1{
                padding-bottom: 20px;
            }

            p{
                line-height: 2;
            }
        }

        &__right{
            width: calc(100% / 2 - 200px);
        }
    }
}
.main__second__content__bottom__instructors{
    height: 520px;
    width: 100%;
    display: flex;
    justify-content: space-between;
}
.main__second__content__bottom__instructors__cards{
    width: calc(100% / 3 - 20px);
    height: 500px;
    background-color: #fff;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    border-radius: 15px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-direction: column;
    padding: 50px;
    color: var(--color__cube__tundora);

    img{
        width: 100%;
        height: auto;
    }
    p{
        text-align: center;
        line-height: 2;
    }
    
    &:hover{
        width: calc(100% / 3 - 10px);
        height: 520px;
    }
    .instructor__name{
        font-weight: 500;
    }
    .instructors__icons{
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 100px;

        .fa-facebook-f, .fa-twitter, .fa-instagram{
            color: var(--color__cube__tundora);
            font-size: 20px;
        }
    }
}
/*--- Buttons ---*/
.main__top__button{
    width: 400px;
    height: 50px;
    outline: none;
    cursor: pointer;
    text-align: center;
    text-decoration: none;
    color: #fff;
    padding: 15px 50px;
    background: var(--color__cube__BayLeaf);
    border: none;
    border-radius: 30px;
    border: solid 2px var(--color__cube__BayLeaf);

    .main__top__button__text{
        text-transform: uppercase;
        font-weight: 700;
        font-size: 15px;
    }
}
.main__top__button:hover{
    background: var(--color__cube__wite);
    transition: 0.3s;
    border: solid 2px var(--color__cube__BayLeaf);
    color: var(--color__cube__BayLeaf)
}
.testimonials{
    width: 100%;

    &___container{
        width: 100%;
        padding: 150px 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        color: var(--color__cube__tundora);

        img{
            width: 200px;
            padding-bottom: 20px;
        }
        .testimonials__coments, .testimonials__name{
            padding: 0 300px;
            font-size: 18px;
            text-align: center;
            font-style: italic;
            line-height: 2;
        }
        .testimonials__name{
            padding: 30px;
            font-weight: 500;
            font-style: normal;
        }
        .comments{
            margin-top: 20px;
            margin-bottom: 50px;
            font-size: 18px;
        }
    }
}
</style>