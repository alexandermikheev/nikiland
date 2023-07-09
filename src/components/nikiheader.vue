
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
                <a href="#slogan"><li  class="navbar-item">ГЛАВНАЯ</li></a>
                <a href="#services-box"><li class="navbar-item">УСЛУГИ</li></a>
                <a href="#price"><li class="navbar-item">ПРАЙС</li></a>
                <a href="#promotions"><li class="navbar-item">АКЦИИ</li></a>
                <a href="#rules"><li class="navbar-item">ПРАВИЛА</li></a>
                <a href="#about"><li class="navbar-item">ПАРТНЁРАМ</li></a>
            </ul>
        </nav>
    </div>
</div>
</template>
<script >
 methods:{

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
    color: red;
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

@media (max-width: 640px) {

 }
@media (min-width: 641px) and (max-width: 1200px) {
    .phone{

        padding-right: 80px;
    }
}
@media (min-width: 1201px) {}

</style>