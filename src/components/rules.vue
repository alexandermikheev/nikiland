<script >

</script>

<template>
<div id="rules">
    <div class="rules-header">правила посещения</div>
</div>
<div class="rules-card">
    <div class="rusles-card-box">
        <div class="rusles-card-logo"><img src="../assets/Rules-logo.svg" alt="" srcset=""></div>
        <div class="rusles-card-button">информация по <a href="НИКИ_ЛЭНД_правила_посещения.pdf">ссылке</a></div>
    </div>
</div>
</template>

<style >
.rules-card{
    background: url(../assets/Oblako1.svg) 0% 50%/30% no-repeat,url(../assets/Oblako2.svg) 100% 0%/30% no-repeat ;
    padding: 131px 0;
}
.rusles-card-box{
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    align-content: center;
    background-position: center center;
    width: 80%;
    margin: auto;
}
.rusles-card-list{
    display: flex;
    flex-direction: column;
    align-items: center;
}
.rusles-card-button{
    color: #695C91;
    font-family: PoetsenOne;
    font-size: 39px;
    font-style: normal;
    font-weight: 400;
    line-height: 140%;
}
.rusles-card-button a{
    color: #F7C400;

}
.rusles-card-item{
    color: #676190;
    font-family: Montserrat;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 111%;
    letter-spacing: -0.09px;
}


@media (min-width: 1201px) {}
@media (min-width: 641px) and (max-width: 1200px) {
    .rules-card{
        background: url(../assets/Oblako1.svg) 0% 50%/30% no-repeat,url(../assets/Oblako2.svg) 100% 0%/30% no-repeat ;
    }
}
@media (max-width: 640px) {
    .rusles-card-button{
        text-align: center;
    }

}
@media (min-width: 376px) and (max-width: 425px){

    .rules-card{
        padding: 44px 0;
    }
    .rusles-card-button{
        text-align: center;
        font-size: 16px;
    }

}
@media (min-width: 320px) and (max-width: 375px){
    .rules-card{
        padding: 44px 0;
    }
    .rusles-card-button{
        text-align: center;
        font-size: 16px;
    }
    
    }
</style>




