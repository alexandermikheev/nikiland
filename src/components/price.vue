<script >

</script>

<template>
<div id="price">
    <h2 class="price-header">
        ПРАЙС
    </h2>
    <div class="price-card">
        <div class="price-card-list">
            <div class="weekdays">
                <h3 class="price-card-list-header">Прайс лист</h3>
                <h3 class="weekdays-header">в будние дни</h3>
                <div class="cost">30 мин - 300₽</div>
                <div class="cost">1 час - 450₽ </div>
            </div>
            <div class="weekends">
                <h3 class="weekends-header">в выходные дни</h3>
                <div class="cost">30 мин - 400₽</div>
                <div class="cost">1 час - 550₽</div>
            </div>
            <div class="smail-grut-fil"></div>
            <div class="cloud"></div>
            <div class="cloud1"></div>
            
        </div>
        <div class="price-card-aboniment">
            <h3 class="price-card-aboniment-header">Абонемент</h3>
            <div class="price-card-aboniment-quantity">
                <span>10</span>
                <h3 class="card-aboniment-header">Сеансов</h3>
                <p class="card-aboniment-header-paragraf">10 посещений по (1часу)-4500₽</p>
            </div>
            <div class="smail-grut-blue"></div>
        </div>

    </div>
    <div class="price-footer">
        <div class="price-footer-header">
            <h2>территория радости и веселья</h2>
        </div>
        <div class="footer-back"></div>
    </div>
</div>
</template>

<style>
.price-card{
    display: flex;
    justify-content: space-evenly;
    margin-bottom: 337px;
    height: 400px;
}

.price-card-list{
    background-image: url(../assets/oblako.svg);
    background-position: center center;
    background-repeat: no-repeat;
    width: 425px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #FFFFFF;
    font-family: Montserrat;
    font-size: 24px;
    font-weight: bold;
    position: relative;

}
.price-card-aboniment-quantity span{
    border-radius: 100%;
    padding: 30px 30px;
    background-color: #8AC8E5;
    display: block;
}
.weekdays-header {
   display: flex;
   flex-direction: column;
}
.price-card-aboniment{
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    justify-content: flex-end;
}
.price-card-aboniment-header, .card-aboniment-header{
    font-family: 'PoetsenOne';
    color: #676091;
    font-size: 38px;

}
.price-card-aboniment-header{
    margin-top: 32px;
    margin-bottom: 32px;
}
.card-aboniment-header{
    margin-top: 17px;
    margin-bottom: 13px;
}
.card-aboniment-header-paragraf{
    font-family: 'Montserrat-ex-bold';
    font-size: 16px;
    color: #8AC8E5;
    font-weight: bold;
    margin: 0;
}
.price-card-aboniment-quantity{
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #676091;
}

.price-card-aboniment-quantity span{
    font-family: 'PoetsenOne';
    font-size: 84px;
}


.smail-grut-fil{
    position: absolute;
    background: url(../assets/smail-grut-fil.svg);
    width: 299px;
    height: 338px;
    top: 400px;
    left: -140px;
}
.smail-grut-blue{
    position: absolute;
    background: url(../assets/smail-grut-blue.svg);
    width: 340px;
    height: 338px;
    top: 400px;
    left: -310px;
}
.cloud{
    position: absolute;
    background: url(../assets/cloud.svg);
    width: 27.975px;
    height: 21.415px;
    top: 530px; 
    left: 110px;
}
.cloud1{
    position: absolute;
    background: url(../assets/cloud.svg);
    background-repeat: no-repeat;
    background-size: contain;
    width: 60px;
    height: 45px;
    top: 450px; 
    left: 160px;
}
.price-card-list-header{
    margin: 0;
    font-size: 26px;
    text-align: center;
    text-transform: uppercase;
    line-height: 38.6px;
}
.weekdays-header, .weekends-header{
    margin: 0;
    color: #676091;
    font-size: 16px;
    line-height: 35.6px;
}
.cost{
    font-size: 28px;
    font-weight: bolder;
    font-family: "Montserrat-bold";
    font-weight: bold;
    line-height: 30px;
}
.cost:nth-child(n+2){
    margin-bottom: 5px;
}
.price-footer{
    height: 170px;
    display: flex;
    background-color: #676091;
    align-items: center;
    justify-content: first baseline;
    position: relative;
}
.price-footer-header{
    color: #FFFFFF;
    font-family: 'PoetsenOne-bold';
    font-size: 32px;
    margin-left: 10%;
}
.footer-back{
    position: absolute;
    background: url(/src/assets/price-footer/smail-blue.svg) bottom left no-repeat, url(/src/assets/price-footer/smail-fil.svg) 72% 19% no-repeat, url(/src/assets/price-footer/smail-j.svg) 93% bottom no-repeat;    height: 200px;
    width: 100%;
    top: -18%;
}
</style>