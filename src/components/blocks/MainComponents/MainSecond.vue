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
                        <img :src="testimonials[currentIndex].img">
                        <p class="testimonials__coments">{{testimonials[currentIndex].Comment}}</p>
                        <p class="testimonials__name">{{testimonials[currentIndex].name}}</p>
                        <div class="thumbs__testimonials">
                            <div class="thumb__on__left" v-on:click="PrevTestimonial()">
                                <i class="fa-regular fa-circle-left"></i>
                            </div>
                            <div class="thumb" v-for="(testimonial, indexTestimonials) in testimonials" :key="indexTestimonials" :class="currentIndex === indexTestimonials ? `active` : null" v-on:click="ChangeTestimonial(indexTestimonials)"></div>
                            <div class="thumb__on__right" v-on:click="NextTestimonial()">
                                <i class="fa-regular fa-circle-right"></i>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="latest">
                    <h1 class="latest__title">Latest News</h1>
                    <div class="latest__content">
                        <div class="latest__content__include" v-for="(latest, indexLatest) in latests" :key="indexLatest">
                            <img :src="latest.image">
                            <h2 class="latest__title">
                                {{latest.title}}
                            </h2>
                            <div class="latest__date__update">
                                <p class="latest__date">{{latest.date}}</p>
                                <p class="latest__comments"> | {{latest.comments}} comments</p>
                                <p class=""></p>
                            </div>
                            <p class="latest__text">{{latest.text}}</p>
                        </div>
                    </div>
                    <button class="latest__button"><p class="latest__button__text">More from the blog</p></button>
                </div>
            </div>
            
        </div>
        <div class="main__fourth">
    
        </div>
    </div>
</template>

<script>
export default {
    name: 'BaseSecond',
    data(){
        return{
            currentIndex: 0,
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
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, ducimus nemo, pariatur voluptatem nulla magni, incidunt quis exercitationem saepe cupiditate aliquam fuga quod! Autem tempora.',
                },
                {
                    name: 'Harold Poping',
                    img: require('../../../assets/img/testimonials/testimonial-harold.png'),
                    Comment: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eum maiores ea obcaecati recusandae voluptatum alias, exercitationem minus labore veritatis voluptate autem, ipsa error.',
                },
                {
                    name: 'Kate Dash',
                    img: require('../../../assets/img/testimonials/testimonial-kate.png'),
                    Comment: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt deleniti veniam libero eaque beatae. Distinctio, deleniti fugiat aut eligendi saepe, voluptatum laborum dolor assumenda hic culpa.',
                },
                {
                    name: 'Kelly Kiely',
                    img: require('../../../assets/img/testimonials/testimonial-kelly.png'),
                    Comment: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde libero pariatur beatae accusamus vero molestiae iure ipsum voluptatibus incidunt, assumenda quaerat quis voluptatum alias.',
                },
                {
                    name: 'Grant Hot',
                    img: require('../../../assets/img/testimonials/testimonial-grant.png'),
                    Comment: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum quasi quis qui, nulla dicta, porro sequi nihil maxime aliquam nesciunt voluptatem placeat. Magni porro saepe praesentium.',
                },
                
            ],
            latests: [
                {
                    image: require('../../../assets/img/latesnews/blog-choosecar-700x441.jpg'),
                    title: 'What car to start with?',
                    date: 'February 7th, 2019',
                    comments: '0',
                    text: 'Lorem ipsum dolor sit amet consectetur!'
                },
                {
                    image: require('../../../assets/img/latesnews/blogpost-10and2-700x441.jpg'),
                    title: 'Avada Driving School Expanding',
                    date: 'February 7th, 2019',
                    comments: '0',
                    text: 'Consecteturipsum dolor sit amet consectetur Lorem.'
                },
            ]
        }
    },
    created() {
        setInterval(() => {
            this.NextTestimonial();
        }, 3000);
    },
    methods: {
        PrevTestimonial(){
            if(this.currentIndex === 0){
                this.currentIndex = this.testimonials.length - 1;
            } else {
                this.currentIndex--;
            }
        },
        NextTestimonial(){
            if(this.currentIndex === this.testimonials.length - 1 ){
                this.currentIndex = 0;
            } else {
                this.currentIndex++;
            }
        },
        ChangeTestimonial(indexTestimonials){
            this.currentIndex = indexTestimonials;
        }
    },
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
    max-height: 850px;
    display: flex;
    justify-content: center;
    background-image: url(../../../assets/img/testimonials/testimonial-background.jpg);
    background-size: cover;

}
.main__fourth{
    width: 100%;
    height: 800px;
    background-image: url(../../../assets/img/latesnews/latestnews-background.jpg);
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
    border-top: 6px solid var(--color__cube__BayLeaf);
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

.latest__button{
    width: 300px;
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

    .latest__button__text{
        text-transform: uppercase;
        font-weight: 700;
        font-size: 15px;
    }
}
.latest__button:hover{
    background: var(--color__cube__wite);
    transition: 0.3s;
    border: solid 2px var(--color__cube__BayLeaf);
    color: var(--color__cube__BayLeaf)
}

/*--- F.Buttons ---*/
.testimonials{
    width: 100%;

    &___container{
        width: 100%;
        padding-top: 150px;
        padding-bottom: 50px;
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
            padding: 20px;
            font-weight: 500;
            font-style: normal;
        }
        .comments{
            margin-top: 20px;
            margin-bottom: 50px;
            font-size: 18px;
        }
        .thumb__on__left, .thumb__on__right {
            margin: 0 20px;
            width: 20px;
            height: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
}

.thumbs__testimonials{
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.thumb{
    width: 18px;
    height: 18px;
    border-radius: 50%;
    border: 1px solid var(--color__cube__tundora);
    margin: 0 5px;
}
.active{
    background-color: var(--color__cube__tundora);

}

/*Latest*/
.latest{
    width: 100%;
    height: 700px;
    border-top: 10px solid var(--color__cube__seagull);
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;
    background-color: #fff;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);

    &::after{
        content: '';
        margin-top: 690px;
        position: absolute;
        width: 100%;
        height: 120px;
        background-image: url(../../../assets/img/latesnews/latestnews-bottom.png);
        background-size: 100%;
        background-repeat: no-repeat;
        
    }

    &__title{
        padding-top: 50px;
        padding-bottom: 40px;
    }
    &__content{
        display: flex;
        width: 100%;
        padding: 0 50px;
        margin-bottom: 50px;

        &__include{
            width: 100%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;

            img{
                width: 500px;
            }

            .latest__title{
                color: var(--color__cube__BayLeaf);
                padding: 20px 0;
                font-weight: 600;
            }
            .latest__date__update{
                display: flex;
                align-items: center;
                color: var(--color__cube__tundora);
                padding-bottom: 20px;
                font-size: 14px;
            }
            .latest__comments{
                color: var(--color__cube__BayLeaf);
                margin-left: 6px;
            }
            .latest__text{
                color: var(--color__cube__tundora);
            }


        }
    }

    .latest__content__title{

    }
}
</style>