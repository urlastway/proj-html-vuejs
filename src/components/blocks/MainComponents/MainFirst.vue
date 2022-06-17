<template>
  <div class="main__first">
    <div class="container">
        <div class="main__content">
            <div class="main__content__top">
                <div class="main__content__top__left">
                    <h1>Start Learning to Drive Today</h1>
                    <h3>Give us a call to shedule your first driving lesson</h3>
                </div>
                <div class="main__content__top__right">
                    <i class="fa-solid fa-phone-flip"></i>
                    <p class="number">1-800-555-555</p>
                </div>
            </div>
            <div class="main__content__bottom">
                <div class="main__content__bottom__left">
                    <div class="courses__left">
                        <div class="courses__left__content">
                            <h1 class="title">Courses</h1>
                            <p class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi obcaecati expedita fugiat vitae nobis omnis quibusdam ducimus, ab dolorum nemo.</p>
                            <button class="courses__left__button"><p class="courses__left__button__text">Course Information</p></button>
                        </div>
                    </div>
                </div>
                <div class="main__content__bottom__right">
                    <div class="right__content" v-for="(property, index) in propertys" :key="index">
                        <img :src="property.image">
                        <p>{{property.title}}</p>
                        <button class="right__bottom__button"><span class="right__bottom__button__text">{{property.buttonName}}</span></button>
                    </div>
                </div>
            </div>
            <div class="main__grafics ">
                <div class="main__grafics__content" v-for="(circle, index) in circles" :key="index">
                    <div class="grafic">
                        <div class="circle__progress">
                            <div class="percents">
                                {{circle.percent}}%
                            </div>
                        </div>
                        <svg class="progress__ring" width="270" height="270">
                            <circle class="progress__ring__circle" stroke="#79b27b" stroke-width="14px"
                            cx="135" cy="135" r="128.5" fill="transparent"/>
                        </svg>  
                    </div>                  
                    <span class="percents__text">{{circle.text}}</span>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>

/*import setProgress from 'methods'*/

export default {
    name: 'MainFirst',
    data(){
        return {
            propertys: [
                {
                    title: 'Pass Plus',
                    image: require('./img/CoursesPassplus.jpg'),
                    buttonName: 'learn More',
                },
                {
                    title: 'Intensive Coure',
                    image: require('./img/CourseIntensive.jpg'),
                    buttonName: 'learn More',
                },
                {
                    title: 'Instructions',
                    image: require('./img/CoursesInstructor.jpg'),
                    buttonName: 'learn More',
                },
            ],
            circles: [
                {
                    percent: '95',
                    text: 'Pass Rate',
                },
                {
                    percent: '100',
                    text: 'Referral Rate',
                },
                {
                    percent: '0',
                    text: 'Accident Rate',
                },
            ]
        };
    },
    created () {
    window.addEventListener('scroll', this.handleScroll);
    },
    methods: {
        /*handleScroll(){
            const circle = document.querySelector('.progress__ring__circle');
            const radius = circle.r.baseVal.value;
            const circumference = 1.5 * Math.PI * radius;
            
            circle.style.strokeDasharray = `${circumference} ${circumference}`;
            circle.style.strokeDashoffset = circumference;

            console.log(radius, circumference);

            setProgress((percent) => {
                const offset = circumference - percent / 100 * circumference;
                circle.style.strokeDashoffset = offset;
            });


            setProgress(this.circles.percent)*/

        },
    }

</script>

<style lang="scss" scoped>

/*--- TOP ---*/
.main__first{
    width: 100%;
    display: flex;
    justify-content: center;
}
.main__content__top{
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

/*--- BOTTOM ---*/


.main__content__bottom{
    width: 100%;
    display: flex;

    &__left{
        width: calc(100% / 4 + 150px);

        .courses__left{
            width: 100%;
            height: 435px;
            background-color: #fff;
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            position: relative;
            box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);

            & img{
                width: 70px;
                height: auto;
                border-top-left-radius: 10px;
                align-self: flex-start;
                justify-self: flex-start;
            }

            &__content{
                width: 100%;
                height: 435px;
                padding: 0 20px;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                color: var(--color__cube__tundora);
            }
            .title{
                font-size: 40px;
                font-weight: 600;
                margin-bottom: 30px;

            }
            .subtitle{
                font-size: 18px;
                line-height: 2;
                text-align: center;
            }
        }
        .courses__left::before{
            width: 100px;
            height: 100px;
            background-image: url(../../../assets/img/learning__drive/new-corner.jpg);
            background-size: cover;
            border-top-left-radius: 10px;
            content: '';
            position: absolute;
            background-repeat: no-repeat;
            padding: 0;
        }
    }
    &__right{
        width: calc(100% - (100% / 4 + 150px));
        height: 430px;
        display: flex;
        align-items: flex-end;

        .right__content{
            width: calc(100% / 3);
            margin-left: 40px;
            color: var(--color__cube__seagull);
            display: flex;
            flex-direction: column;
            align-items: center;

            img{
                width: 100%;
                margin-bottom: 10px;
            }

            p{
                font-size: 22px;
                font-weight: 500;
            }

        }
    }
}

/*--- F.BOTTOM RIGHT ---*/



/*--- F.BOTTOM ---*/

/*--- BUTTONS ---*/
.courses__left__button {
    margin-top: 20px;
    outline: none;
    cursor: pointer;
    text-align: center;
    text-decoration: none;
    color: #fff;
    padding: 15px 20px;
    background: var(--color__cube__BayLeaf);
    border: none;
    border-radius: 15px;
    border: solid 2px var(--color__cube__BayLeaf);

    .courses__left__button__text{
        text-transform: uppercase;
        font-weight: 700;
        font-size: 15px;
    }

    }
.courses__left__button:hover{
        background: var(--color__cube__wite);
        transition: 0.3s;
        border: solid 2px var(--color__cube__BayLeaf);
        color: var(--color__cube__BayLeaf)
    }
.right__bottom__button{
    margin-top: 10px;
    outline: none;
    cursor: pointer;
    text-align: center;
    text-decoration: none;
    color: var(--color__cube__seagull);
    padding: 10px 14px;
    border: none;
    border-radius: 30px;
    border: solid 2px var(--color__cube__seagull);

    .right__bottom__button__text{
        font-size: 12px;
        text-transform: uppercase;
    }
}
.right__bottom__button:hover{
        background: var(--color__cube__seagull);
        transition: 0.3s;
        border: solid 2px var(--color__cube__seagull);
        color: var(--color__cube__wite)
    }
/*--- MAIN GRAFICS ---*/
.main__grafics{
    margin: 100px 0;
    width: 100%;
    display: flex;
    justify-content: space-between;

    &__content{
        margin-top: 50px;
        width: calc(100% / 3 - 60px);
        height: 450px;
        background-color: #fff;
        border-radius: 15px;
        position: relative;
        box-shadow: 0 -10px var(--color__cube__BayLeaf);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);

    }
    .grafic{
        display: flex;
        flex-direction: column;
        justify-content: center;


        .circle__progress{
            width: 270px;
            height: 270px;
            border-radius: 50%;
            background-color: rgba(180, 180, 180, 0.514);
            display: grid;
            place-items: center;
            position: relative;

            .percents{
                position: relative;
                font-size: 50px;
                color: var(--color__cube__BayLeaf);
            }

            }

        .circle__progress::before{
            width: 90%;
            height: 90%;
            position: absolute;
            border-radius: 50%;
            background-color: #fff;
            content: '';
        }
        .progress__ring{
            position: absolute;
        }
        .progress__ring__circle{
            transform-origin: center;
            transform: rotate(-90deg);
            stroke-dasharray: 750;            
        }

    }
    .percents__text{
            color: var(--color__cut__gumbo);
            font-size: 20px;
            padding-top: 20px;
        }
}
</style>