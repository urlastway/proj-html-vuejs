<template>
    <div class="header__inner">
        <div class="container">
            <div class="header__inner__content">
                <div class="header__inner__left">
                <h1 class="header__inner__left__title"> Drive width Avada</h1>
                <h2 class="header__inner__left__subtitle">We offer the dinest driving tuition money can buy</h2>
            </div>
            <div class="header__inner__right">
                <div class="header__inner__right__top__box">
                    <i class="fa-solid fa-car"></i >
                    <p class="box__text">Demos</p>
                </div>
                <div class="header__inner__right__buttom__box">
                    <div class="box__price">
                        <i class="fa-solid fa-dollar-sign"></i>
                        <p class="box__price__show">39</p>
                    </div>
                    <p class="box__text">On Sale</p>
                </div>
            </div>
            </div>
         </div>
    </div>
</template>

<script>
export default {
    name: 'BaseFooter',
}
</script>

<style lang="scss" scoped>
.header__inner{
    width: 100%;
    height: 650px;
    display: flex;
    justify-content: center;
    color: var(--color__cube__wite);

    &__left{
        width: calc(100% / 2);
        padding-top: 300px;    
        
        &__title{
            font-size: 3rem;
        }

        &__subtitle{
            padding-top: 25px;
            font-weight: 300;
            font-size: 1.5rem;
        }
    };
    &__content{
        display: flex;
    }
    &__right{

        width: calc(100% / 2);
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        color: var(--color__cube__firefly);

        &__top__box{
            margin-bottom: 10px;
        }
        &__top__box, &__buttom__box{
            width: 70px;
            height: 70px;
            background-color: var(--color__cube__wite);
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    }
    .box__text{
        font-weight: 600;
        color: var(--color__cube__tundora);
        font-size: 14px;
    }
    .fa-car{
        font-size: 36px;
        color: var(--color__cube__tundora);
    }
    .box__price{
        display: flex;

        &__show{
            font-weight: 700;
            font-size: 28px;
        }

        .fa-dollar-sign{
            font-size: 18px;
        }

        &__show, .fa-dollar-sign{
            color: var(--color__cube__BayLeaf);
        }

    }

}
</style>