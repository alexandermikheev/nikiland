<template>
    <div class="footer">
        <div class="footer-box">
        <div class="footer-logo"></div>
        <div class="footer-phone">
            <a class="footer-phone-tel footer-elem" href="tel:+79256270456">8-925-627-04-56</a>
            <a class="footer-elem" href="mailto:info@nikiland.club">info@nikiland.club</a>
            <div class="footer-social footer-elem">
                <ul class="footer-social-items"> 
                    <a href="tel:+79256270456"><li class="footer-social-item"><img src="../assets/header/phone1.svg" alt="phone"></li></a>
                    <a href="wtsp.cc/79256270456"><li class="footer-social-item"><img src="../assets/header/whatsapp-logo1.svg" alt="wa"></li></a>
                    <a href="https://t.me/89256270456"><li class="footer-social-item"><img src="../assets/header/telegram-logo1.svg" alt="telegram"></li></a>
                    <a href="https://instagram.com/nikiland.club?igshid=MzRlODBiNWFlZA=="><li class="footer-social-item"><img src="../assets/header/Vector.svg" alt="instagram"></li></a>
                </ul>
            </div>

        </div>
    </div>
    <div class="lic"><span>© 2023 "НИКИ ЛЭНД". Все права защищены.</span></div>
    </div>

</template>
<style>
.footer ul {
    list-style-type: none;
}
.footer{
    display: flex;
    padding-top: 40px;
    flex-direction: column;
    align-items: center;
    box-shadow: 0px 0px 34px 2px rgba(34, 60, 80, 0.13);
    margin-top: 40px;
    box-sizing: border-box;
}
.footer-box{
    display: flex;
    align-items: center;
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
.footer-phone a:hover{
    color: #695C91;
}
.footer-phone{
    display: flex;
    align-content: center;
    align-items: center;
}
.footer-elem:nth-child(n+1){
    margin-left: 52px;
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
.footer-social-items a:nth-child(n+2):nth-last-child(n+1){
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
.lic{
    display: flex;
    width: 100%;
    max-width: 1160px;
    justify-content: end;
    color: #C4C4C4;
    font-family: Montserrat;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 131%; /* 20.96px */
    text-decoration-line: underline;
}
.footer-logo{
    background: url(../assets/footer-logo.svg) no-repeat;
    height: 97px;
    width: 391px;
}

@media (min-width: 641px) and (max-width: 1200px) {
    .footer-phone {
    display: flex;
    align-content: center;
    margin-left: 8px;
    margin-right: 0; 
    flex-direction: column;
}
.footer-logo{
    background: url(../assets/Rules-logo.svg) no-repeat;
    height: 150px;
    width: 176px;
}
}

@media (max-width: 640px) {
    .footer-phone {
    display: flex;
    align-content: center;
    margin-left: 8px;
    margin-right: 0; 
    flex-direction: column;
}
.footer-logo{
    background: url(../assets/Rules-logo.svg) no-repeat;
    height: 150px;
    width: 176px;
}
.footer-elem:nth-child(n+1){
    margin-left: 0px;
}
.footer-phone a{
    font-size: 16px;
}
}




@media (min-width: 376px) and (max-width: 425px){
    .footer-phone {
    display: flex;
    align-content: center;
    margin-left: 8px;
    margin-right: 0; 
    flex-direction: column;
}
.footer {
    margin: 0 5px;
 }
 .footer-logo{
    background: url(../assets/Rules-logo.svg) no-repeat;
    height: 150px;
    width: 176px;
}
.footer-elem:nth-child(n+1){
    margin-left: 0px;
}
.footer-phone a{
    font-size: 16px;
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
 .footer-box{
    width: 100%;
}
 .footer-logo{
    background: url(../assets/Rules-logo.svg) no-repeat;
    height: 150px;
    width: 176px;
}
.footer-elem:nth-child(n+1){
    margin-left: 0px;
}
.footer-phone a{
    font-size: 16px;
}
}
</style>