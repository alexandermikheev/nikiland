<template>
    <header class="header" v-bind:class="{opened:isOpened}">
        <div class="container header__container">

            <a href="#" class="logo">
                <img class="logo__img" src="../assets/header/лого.svg" alt="Логотип">
            </a>
            <button @click="openMenu" class="header__burger-btn"  id="burger">
                <span></span><span></span><span></span>
            </button> 
            <nav class="menu">
                <ul class="menu__list">
                    <li v-for="(item, index) in menuItems" :key="index" class="menu__item">
                        <a @click="closeMenu"  class="menu__link" :href="item.link">
                            {{ item.name }}
                        </a>
                    </li>
                </ul>
            <div class="phone">
            <a class="phone-tel" href="tel:+79256270456">8-925-627-04-56</a>
            <a class="mail" href="mailto:info@nikiland.club">info@nikiland.club</a>
            <div class="social">
                <ul class="social-items"> 
                    <a href="tel:+78008008080"><li class="social-item phone-mob"><img src="../assets/header/phone1.svg" alt="phone"></li></a>
                    <a href="https://wtsp.cc/78008008080"><li class="social-item wa"><img src="../assets/header/whatsapp-logo1.svg" alt="wa"></li></a>
                    <a href="https://t.me/88008008080"><li class="social-item telegram"><img src="../assets/header/telegram-logo1.svg" alt="telegram"></li></a>
                    <a href="https://instagram.com/nikiland.club?igshid=MzRlODBiNWFlZA=="><li class="social-item instagram"><img src="../assets/header/Vector.svg" alt="instagram"></li></a>
                </ul>
            </div>
            </div>

            </nav>
        </div>
    </header>
</template>
    
<style>
html {
    box-sizing: border-box;
}

*,
*::before,
*::after {
    box-sizing: inherit;
}

a {
    color: inherit;
    text-decoration: none;
}

img {
    max-width: 100%;
}

body {
    font-family: Arial, Verdana, sans-serif;
}

.container {
    /* max-width: 1200px; */
    margin: 0 auto;
    padding: 0 15px;
}

.header {
    box-shadow: 0px 4px 21px -1px rgba(34, 60, 80, 0.13);
    background: url(../assets/header/shar.svg) top left no-repeat, url(../assets/header/blue.svg) top right no-repeat;
    z-index: 99;
    top: 0;
    width: 100%;
    background-color: white;
    position: fixed;
}

.header__container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-top: 10px;
    padding-bottom: 10px;
}

.header__burger-btn {
    display: none;
    position: relative;
    width: 50px;
    height: 50px;
    border: none;
    background-color: transparent;
    z-index: 2;
}

.header__burger-btn span {
    position: absolute;
    width: 40px;
    height: 3px;
    background-color: black;
    left: 5px;
    transition: transform .5s, opacity .5s, background-color .5s;
}

.header__burger-btn span:nth-child(1) {
    transform: translateY(-10px);
}

.header__burger-btn span:nth-child(3) {
    transform: translateY(10px);
}

.header.opened .header__burger-btn span {
    background-color:#695C91;
;
}

.header.opened .header__burger-btn span:nth-child(1) {
    transform: translateY(0) rotate(45deg);
}

.header.opened .header__burger-btn span:nth-child(2) {
    opacity: 0;
}

.header.opened .header__burger-btn span:nth-child(3) {
    transform: translateY(0) rotate(-45deg);
}

.logo {
    display: block;
}

.logo__img {
    width: 200px;
}
.menu{
    display: flex;
    flex-direction: column-reverse;
}
.menu__list {
    display: flex;
    align-items: center;
    list-style-type: none;
    padding: 0;
    margin: 0;
    color: #9D9D9D;
    font-family: 'Montserrat';
    font-size: 24px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}

.menu__item:not(:last-child) {
    margin-right: 44px;
}
.menu__item:hover{
    color: #695C91;
}

.phone{
    display: flex;
    align-items: end;
    flex-direction: column;
    color: #9D9D9D;
    font-size: 24px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    margin-bottom: 10px;
}
.phone-tel{
    font-size: 24px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    text-decoration: none;
    color: #9D9D9D;
}
.mail{
    display: none;
    font-size: 24px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    text-decoration: none;
    color: #9D9D9D;
}
.social-items{
    display: flex;
    list-style-type: none;
    color: #9D9D9D;
    font-size: 24px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    margin: 0;
    padding: 0;
}
.social-items a:nth-child(n+2):nth-last-child(n+1){
    box-sizing: border-box;
    padding-left: 25px;
}
@media (min-width: 1201px) {}

@media (min-width: 641px) and (max-width: 1200px) {
    .header{
        box-shadow: 0px 4px 21px -1px rgba(34, 60, 80, 0.13);
        background: url(../assets/header/shar.svg) top left no-repeat;
        background-color: white;
    }
    .header .menu {
        transform: translateX(100%);
    }
    .header__burger-btn {
        display: block;
    }
    .logo{
        margin-right: 35%;
    }
    .menu {
        position: fixed;
        left: -2px;
        top: 0;
        width: 101%;
        padding: 75px 20px 20px 20px;
        transition: transform .5s;
        height: 100%;
        background: url(../assets/header/menu-smail.svg) 66% 42%/35% no-repeat;
        background-color: #9D9D9D;
        display: block;
        overflow: auto;
    }
    .menu__list {
        display: block;
    }
    .menu__item{
        height: 67.53px;
    }
    .menu__item a:hover{
        color: #695C91;
    }
    .menu__link {
        color: #FFF;
        font-family: Montserrat;
        font-size: 29px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
    }
    .header.opened .menu {
        transform: translateX(0%);
    }
    .phone{
        display: flex;
        align-items: start;
        flex-direction: column;
        color: white;
        font-size: 4.4vw;
        font-family: "Montserrat";
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        padding-top: 0;
        }
    .phone-tel{
        color: #FFF;
        font-family: "Montserrat";
        font-size: 23px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        text-decoration: none;
        padding-bottom: 10px;
        }
  
        .mail{
        display: block;
        color: #FFF;
        font-family: "Montserrat";
        font-size: 21px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        text-decoration: none;
        padding: 0 0 20px;
        }    
    .social-items{
        display: flex;
        list-style-type: none;
        color: #9D9D9D;
        font-size: 24px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        margin: 0;
        padding: 0;
        }
        .social-items a:nth-child(n+2):nth-last-child(n+1) {
        box-sizing: border-box;
        padding-right: 29px !important;
        padding-left: 0;
        }
    .phone-mob{
            display: none;
    }
    .wa{
            padding-left: 0px;
    }
    .header__container {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding-top: 10px;
        padding-bottom: 10px;
    }
}
@media (max-width: 640px) {
    .header{
        box-shadow: 0px 4px 21px -1px rgba(34, 60, 80, 0.13);
        background: url(../assets/header/shar.svg) top left no-repeat;
        background-color: white;
    }
    .header .menu {
    transform: translateX(100%);
    }
    .header__burger-btn {
        display: block;
    }
    .logo{
        margin-right: 26%;
    }
    .menu {
        position: fixed;
        left: -2px;
        top: 0;
        width: 101%;
        padding: 75px 20px 20px 20px;
        transition: transform .5s;
        height: 100%;
        background: url(../assets/header/menu-smail.svg) 79% 39%/35% no-repeat;
        background-color: #9D9D9D;
        display: block;
        overflow: auto;
    }
    .menu__list {
        display: block;
    }
    .menu__item{
        height: 11vw;
    }
    .menu__item a:hover{
        color: #695C91;
    }
    .menu__link {
        color: #FFF;
        font-family: Montserrat;
        font-size: 29px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
    }
    .header.opened .menu {
        transform: translateX(0%);
    }
    .phone{
        display: flex;
        align-items: start;
        flex-direction: column;
        color: white;
        font-size: 4.4vw;
        font-family: "Montserrat";
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        padding-top: 20px;
        }
    .phone-tel{
        color: #FFF;
        font-family: "Montserrat";
        font-size: 29px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        text-decoration: none;
        padding: 0 0 10px;
        }
  
        .mail{
        display: block;
        color: #FFF;
        font-family: "Montserrat";
        font-size: 29px;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        text-decoration: none;
        }    
    .social-items{
        display: flex;
        list-style-type: none;
        color: #9D9D9D;
        font-size: 24px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 600;
        line-height: normal;
        margin: 0;
        padding: 20px 0;
        }
    .social-items a:nth-child(n+2):nth-last-child(n+1) {
        box-sizing: border-box;
        padding-right: 29px !important;
        padding-left: 0;
        }
    .phone-mob{
            display: none;
    }
    .wa{
            padding-left: 0px;
    }
    .header__container {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding-top: 10px;
        padding-bottom: 10px;
    }
}

@media (min-width: 376px) and (max-width: 425px){
.logo {
    margin-right: 12%;
}

}

@media (min-width: 320px) and (max-width: 375px){
.logo {
    margin-right: 12%;
}
}


</style>

<script>
export default{
    data() {
        return {
            menuItems:
            [
                {name: 'ГЛАВНАЯ', link: '#slogan'},
                {name: 'УСЛУГИ', link: '#services'},
                {name: 'ПРАЙС',link: '#price'},
                {name: 'АКЦИИ', link: '#promotions'},
                {name: 'ПРАВИЛА', link: '#rules'},
                {name: 'ПАРТНЁРАМ', link: '#about'},
            ],      
            isOpened: false, 
            isNavigationFixed: true,
            isPageMenu: false,
            actualSubMenu: null,
            actualElement: null,
            categories: null,
            namesList: [],
        }
    },
    methods: {
        openMenu(){
            const el = document.body;
            this.isOpened = !this.isOpened;
            if(!this.isOpened){
                el.style.overflow = 'auto';
            }else{
                el.style.overflow = 'hidden';
            }
        },
        closeMenu(){
            const el = document.body;
            el.style.overflow = 'auto';
            this.isOpened = !this.isOpened;
        }
    }
}

</script>
