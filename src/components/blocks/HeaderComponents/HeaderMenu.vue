<template>
  <div class="header__b">
    <div class="container">
        <div class="header__menu">
             <div class="header__menu__left">
                <img src="../../../assets/img/logo/avada-drivers-logo-2x-400x77.png">
            </div>
            <div class="header__menu__right">
                <nav class="header__nav">
                    <ul v-for="(link, index) in links" :key="index">
                        <li>
                            <a :href="link.url" :class="{active : link.current}">
                                <div class="links">
                                    <p class="link">{{link.text}}</p>
                                    <p :class="{right__add : link.new}">{{link.text__new}}</p>
                                </div>
                            </a>
                        </li>
                    </ul>
                </nav>
                <button class="header__button"><p>Book now</p></button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>

export default {
    name: 'BaseMain',
    data(){
        return {
            links: [
                {
                    text:"Home",
                    url: "#",
                    current: true,
                    new: false,
                },
                {
                    text:"About",
                    url: "#",
                    current: false,
                    new: false,
                },
                {
                    text:"Prices",
                    url: "#",
                    current: false,
                    new: false,
                },{
                    text:"Courses",
                    text__new: "new",
                    url: "#",
                    current: false,
                    new: true,
                },{
                    text:"Locations",
                    url: "#",
                    current: false,
                    new: false,
                },
                {
                    text:"Blog",
                    url: "#",
                    current: false,
                    new: false,
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>

@import '../../../assets/Style/mixin.scss';
    .header__b{
        width: 100%;
        height: 100px;
        align-items: center;
        display: flex;
        justify-content: center;
        background-color: rgb(63, 63, 63);

    }
    .header__menu{
        display: flex;
        justify-content: space-between;
        align-items: center;

        &__right{
            display: flex;
            align-items: center;
                ul {
                    @include ComponentsInLine;
                    padding: 0 10px;
                    text-transform: uppercase;
                    
                }
                .active{
                    color: var(--color__cube__BayLeaf);
                    padding-bottom: 5px;
                    border-bottom: solid 2px var(--color__cube__BayLeaf);

                    };
                a{
                    text-decoration: none;
                    font-weight: 700;
                    color: var(--color__cube__wite);
                }
                
                a:hover{
                    color: var(--color__cube__BayLeaf);
                    padding-bottom: 5px;
                    border-bottom: solid 2px var(--color__cube__BayLeaf);

                    .right__add{
                        color: #fff;
                    }
                }
            }
    };
    .header__nav{
        display: flex;
        align-items: center;
        margin: 20px 0;
    };
    /*--- BUTTON ---*/
    .header__button {
        outline: none;
        cursor: pointer;
        text-align: center;
        text-decoration: none;
        color: #fff;
        padding: 10px 20px;
        background: var(--color__cube__BayLeaf);
        border: none;
        border-radius: 15px;

        p{
            text-transform: uppercase;
            font-weight: 700;
            font-size: 15px;
        }

    }
    .header__button:hover{
        background: var(--color__cut__BayLeaf);
        transition: 0.3s;
    }
    .links{
        display: flex;
        align-items: center;

        .right__add{
            margin-left: 10px;
            background-color: var(--color__cube__BayLeaf);
            padding: 7px;
            border-radius: 15px;
            font-size: 12px;
        }
    }

</style>