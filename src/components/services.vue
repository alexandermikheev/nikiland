<template>
    <div id="services">
        <span class="services-header">Услуги</span>
        <div id="services-box">
            <div v-for="(item, index) in serviceitem" :key="index" class="services-card">
                <div class="services-card-item">
                    <div class="services-card-container">
                    <div class="services-img"><img :src="item.src" alt=""></div>
                    <h2 class="services-card-header">{{ item.title }}</h2>
                    <p class="services-card-paragraf">{{ item.deskription }}</p>
                </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script >
export default{
    data() {
        return {
            serviceitem:
            [
                {title: 'ДЕТСКИЙ ЦЕНТР ДЛЯ ДЕТЕЙ ОТ 0 ДО 7 ЛЕТ (ВКЛЮЧИТЕЛЬНО) ИЛИ РОСТОМ ДО 130 СМ', deskription: 'Вы можете вашего ребенка оставить с нашими веселыми и ответственными сотрудниками, если его возраст не менее четырех лет.',src:'service/1.png'},
                {title: 'Красивые фотографии', deskription: 'Профессиональные фотографы детского центра запечатлят самые яркие моменты, а вы сможете приобрести фотографии на память',src:'service/2.png'},
                {title: 'Организация праздников', deskription: 'Наша команда профессионалов поможет организовать яркий, веселый и запоминающийся праздник для Ваших детей.',src:'service/3.png'},
                {title: 'Опытные аниматоры', deskription: 'Профессиональные аниматоры всегда готовы радовать наших гостей увлекательными играми и интересными конкурсами. Большой выбор любимых героев!',src:'service/4.png '},
            ]
        }
    }}
</script>
<style >
#services-box{
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-wrap: wrap;
}
.services-header{
    display: block;
}
.services-card{
    display: flex;
    justify-content: center;
}
.services-card-container{
    width: 259px;
}
.services-card-item{
    margin: 40px;
}
.services-img{
    border-radius: 40px;
    overflow: hidden;
    display: flex;
    justify-content: center;
}
.services-card-header{
    color: #695C91;
    font-size: 14px;
    font-family: "Montserrat-bold";
    font-style: normal;
    font-weight: 700;
    line-height: 139.5%;
    text-transform: uppercase;
    margin-top: 20px;
    margin-bottom: 10px;
}
.services-card-paragraf{
    color: #9D9D9D;
    font-size: 16px;
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    line-height: 139.5%;
}
/* @media (min-width: 641px) and (max-width: 1200px) {

   .services-card{


   }
   .services-card-item{

   }
   } */
</style>