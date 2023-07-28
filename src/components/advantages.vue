<script >

</script>

<template>
<div id="advantages">
    <div class="advantages-header-text">
        <span class="advantages-header" >Наши преимущества</span>
        <span class="advantages-text">Отличительные особенности наших Семейных Центров:</span>
    </div>
    <div class="advantages-list">
        <div class="advantages-items">
            <div class="advantages-item">
                <img src="../assets/advantages/clock.svg" alt="">
                <span>ФИКСИРОВАННАЯ ЧАСОВАЯ ОПЛАТА ИЛИ АБОНЕМЕНТ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/Group.svg" alt="">
                <span>БЕЗОПАСНЫЕ АТТРАКЦИОНЫ ДАЖЕ ДЛЯ САМЫХ МАЛЕНЬКИХ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/Безымянный-4 1.svg" alt="">
                <span>УДОБНОЕ РАСПОЛОЖЕНИЕ В ЦЕНТРЕ ТЦ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/уборка.svg" alt="">
                <span>ЕЖЕДНЕВНАЯ УБОРКА И КОНТРОЛЬ ЗА ЧИСТОТОЙ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/уборка.svg" alt="">
                <span>ЕЖЕДНЕВНАЯ УБОРКА И КОНТРОЛЬ ЗА ЧИСТОТОЙ</span>
            </div>
            <!-- <div class="advantages-item">
                <img class="smail" src="../assets/advantages/смайл.svg" alt="">

            </div> -->
            <div class="advantages-item">
                <img src="../assets/advantages/лошадь.svg" alt="">
                <span>ИГРОВЫЕ МОДУЛИ, АТТРАКЦИОНЫ И ИГРУШКИ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/Безымянный-3 1.svg" alt="">
                <span>ЕЖЕДНЕВНЫЙ ОСМОТР ВСЕХ ИГРОВЫХ МОДУЛЕЙ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/Безымянный-10 1.svg" alt="">
                <span>С ЛЮБОВЬЮ И ЗАБОТОЙ К КАЖДОМУ</span>
            </div>
            <div class="advantages-item">
                <img src="../assets/advantages/Group 44.svg" alt="">
                <span>ОРГАНИЗАЦИЯ ПРАЗДНИКОВ И ДНЕЙ РОЖДЕНИЙ</span>
            </div>
        </div>
    </div>
    <div class="smail smail-1"></div>
    <div class="smail smail-2"></div>
    <div class="smail smail-3"></div>
</div>
</template>

<style >
    #advantages{
        background-image: url(../assets/advantages/back.svg);
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        position: relative;

    }
    .advantages-list{
        border-radius: 60px;
        background: rgba(103, 96, 145, 0.85);
        color: #FFF;
        font-size: 18px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 700;
        line-height: 131%;
        display: flex;
        justify-content: center;
        max-width: 1150px;
        min-width: 315px;
        margin-bottom: 64px;
        padding-top: 30px;
        padding-bottom: 30px;
        box-sizing: content-box;
    }
    .advantages-header-text{
        color: #695C91;
        text-align: center;
        font-size: 32px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 700;
        line-height: 140%;
        text-transform: uppercase;
        padding-bottom: 40px;
        padding-top: 60px;
    }
    .advantages-items{
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        justify-content: space-around;
    }
    .advantages-header-text{
        display: flex;
        flex-direction: column;
    }
    .advantages-item img {
        width: 83px;
        height: 88px;
        margin-right: 10px;
    }
    .advantages-item{
        width: 25%;
        display: flex;
        align-items: center;
        padding: 20px;
    }
    .advantages-header{
        color: #695C91;
        text-align: center;
        font-size: 32px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 700;
        line-height: 140%;
        text-transform: uppercase;
    }
    .advantages-text{
        color: #695C91;
        text-align: center;
        font-size: 17px;
        font-family: Montserrat;
        font-style: normal;
        font-weight: 500;
        line-height: 140%;
        text-transform: lowercase;
    }
    .smail{
        position: absolute;
        width: 50px;
        height: 50px;
        background-repeat: no-repeat;
        background-size: contain;
    }
    .smail-1{
        top: 70%;
        left: 4.2%;
        background-image: url(../assets/advantages/smail1.svg);
        width: 73.006px;
        height: 75.513px;
    }
    .smail-2{
        top: 18%;
        left: 75%;
        background-image: url(../assets/advantages/smail2.svg);
        width: 67.006px;
        height: 69.282px;
    }
    .smail-3{
        top: 40%;
        left: 88%;
        background-image: url(../assets/advantages/smail3.svg);
        width: 77.006px;
        height: 79.627px;
    }
</style>