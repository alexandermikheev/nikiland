
<template>
<div class="header">
    <div class="logo">
        <img src="../assets/header/лого.svg" alt="logoniki">
    </div>
    <div class="navbar">
        <div class="phone">
            <a class="phone-tel" href="tel:+78008008080">8-800-800-80-80</a>
            <div class="social">
                <ul class="social-items"> 
                    <li class="social-item"><img src="../assets/header/phone 1.svg" alt="phone"></li>
                    <li class="social-item"><img src="../assets/header/whatsapp-logo 1.svg" alt="wa"></li>
                    <li class="social-item"><img src="../assets/header/telegram-logo 1.svg" alt="telegram"></li>
                    <li class="social-item"><img src="../assets/header/Vector.svg" alt="instagram"></li>
                </ul>
            </div>
        </div>
        <nav class="navbar-list">
            <ul class="navbar-items">
                <a v-for="(item, index) in menuItems" :key="index" :href="item.link"><li class="navbar-item">{{ item.name }}</li></a>
            </ul>
        </nav>
                <!-- mobile -->
    <div class="burger" >
        <img src="../assets/header/burger_menu/menu.svg" class="burger__but">
    </div>

    <div class="burger__menu" >
        <div class="burger__empty"></div>
        <div class="burger__wrap">
            
        </div>
    </div>
    </div>

</div>
</template>
<script >
export default{
    data() {
        return {
            menuItems:
            [
                {name: 'ГЛАВНАЯ', link: '#slogan'},
                {name: 'УСЛУГИ', link: '#services-box'},
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
    }
</script>
<style >
html{
  scroll-behavior: smooth;
}

.header{
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    padding-top: 22px;
    padding-bottom: 13px;
    border-bottom: 2px solid #9D9D9D;
    background: url(../assets/header/shar.svg) top left no-repeat, url(../assets/header/blue.svg) top right no-repeat;
}
.logo{
    padding-right: 52px;
    width: 180px;
}
.navbar{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
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
.social-items li:nth-child(n+2):nth-last-child(n+1){
    box-sizing: border-box;
    padding-left: 29px;
}
.navbar-list{
    display: flex;
}
.navbar-items{
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
    align-content: end;
    flex-wrap: wrap;
}
.navbar-items a{
    text-decoration: none;
    display: flex;
    color: #9D9D9D;
    flex-wrap: wrap;
}
.navbar-item:hover{
    color: #695C91;
}
.navbar-items a:nth-child(n+2):nth-last-child(n+1){
    box-sizing: border-box;
    padding-left: 44px;
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
}
.phone-tel{
    color: #9D9D9D;
    font-size: 24px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    text-decoration: none;
}

</style>