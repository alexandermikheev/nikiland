<template>
    <div class="footer">
        <div class="footer-logo"><img src="../assets/Rules-logo.svg" alt="logo"></div>
        <div class="footer-phone">
            <a class="footer-phone-tel" href="tel:+78008008080">8-800-800-80-80</a>
            <a href="mailto:info@nikiland.ru">info@nikiland.ru</a>
            <div class="footer-social">
                <ul class="footer-social-items"> 
                    <li class="footer-social-item"><img src="../assets/header/phone 1.svg" alt="phone"></li>
                    <li class="footer-social-item"><img src="../assets/header/whatsapp-logo 1.svg" alt="wa"></li>
                    <li class="footer-social-item"><img src="../assets/header/telegram-logo 1.svg" alt="telegram"></li>
                    <li class="footer-social-item"><img src="../assets/header/Vector.svg" alt="instagram"></li>
                </ul>
            </div>
        </div>
            <nav class="footer-navbar-list">
            <ul class="footer-navbar-items">
                <a href="#slogan"><li  class="footer-navbar-item">ГЛАВНАЯ</li></a>
                
                <a href="#services-box"><li class="footer-navbar-item">УСЛУГИ</li></a>
                <a href="#price"><li class="footer-navbar-item">ПРАЙС</li></a>
                <a href="#rules"><li class="footer-navbar-item">ПРАВИЛА ПОСЕЩЕНИЯ</li></a>
                <a href="#promotions"><li class="footer-navbar-item">АКЦИИ</li></a>

                <a href="#about"><li class="footer-navbar-item">ПАРТНЁРАМ</li></a>

                <a href="#map-ya"><li class="footer-navbar-item">КАРТА</li></a>
                <a href="#reviews"><li class="footer-navbar-item">ОТЗЫВЫ</li></a>

            </ul>      
        </nav>
    </div>
    <div class="lic">© 2023 "НИКИ ЛЭНД". Все права защищены.</div>
</template>
<style>
.footer ul {
    list-style-type: none;
}
.footer{
    display: flex;
    padding-top: 40px;
    justify-content: center;
}
.footer-phone a{
    display: flex;
    color: #9D9D9D;
    font-family: Montserrat;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-decoration: none;
}
.footer-phone{
    display: flex;
    flex-direction: column;
    align-content: center;
    margin-left: 52px;
    margin-right: 92px;
    
}
.footer-navbar-list{
    display: flex;
    width: 526px;
}
.footer-navbar-list ul{
    padding: 0;
}
.footer-social-items{
    display: flex;
    padding: 0;
}
.footer-social-items li:nth-child(n+2):nth-last-child(n+1){
    box-sizing: border-box;
    padding-left: 29px;
}
.footer-navbar-items a{
    color: #9D9D9D;
    font-family: Montserrat;
    font-size: 24px;
    font-weight: 600;
    text-decoration: none;
}
.footer-navbar-items{
    display: flex;
    margin: 0;
    flex-wrap: wrap;
    justify-content: space-between;
}
.footer-navbar-item{
    width: 20%;
}

</style>