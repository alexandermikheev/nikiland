<template>
    <div class="footer">
        <div class="footer-logo"><img src="../assets/Rules-logo.svg" alt="logo"></div>
        <div class="footer-phone">
            <a class="footer-phone-tel" href="tel:+78008008080">8-800-800-80-80</a>
            <a href="mailto:info@nikiland.ru">info@nikiland.ru</a>
            <div class="footer-social">
                <ul class="footer-social-items"> 
                    <li class="footer-social-item"><img src="../assets/header/phone1.svg" alt="phone"></li>
                    <li class="footer-social-item"><img src="../assets/header/whatsapp-logo1.svg" alt="wa"></li>
                    <li class="footer-social-item"><img src="../assets/header/telegram-logo1.svg" alt="telegram"></li>
                    <li class="footer-social-item"><img src="../assets/header/Vector.svg" alt="instagram"></li>
                </ul>
            </div>
            <div class="lic">© 2023 "НИКИ ЛЭНД". Все права защищены.</div>
        </div>
       
    </div>

</template>
<style>
.footer ul {
    list-style-type: none;
}
.footer{
    display: flex;
    padding-top: 40px;
    justify-content: space-around;
    box-shadow: 0px 0px 34px 2px rgba(34, 60, 80, 0.13);
    margin-top: 40px;
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

@media (min-width: 376px) and (max-width: 425px){
    .footer-phone {
    display: flex;
    flex-direction: column;
    align-content: center;
    margin-left: 8px;
    margin-right: 0; 
}
.footer {
    margin: 0 5px;
 }

}

@media (min-width: 320px) and (max-width: 375px){
    .footer-phone {
    display: flex;
    flex-direction: column;
    align-content: center;
    margin-left: 8px;
    margin-right: 0; 
}
.footer {
    margin: 0 5px;
 }

}
</style>