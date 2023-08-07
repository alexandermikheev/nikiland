<script >

</script>

<template>
  <div id="map-ya">
    <div class="map-ya-header">карта семейных центров</div>
    <div class="map-ya-box"> 
      <iframe class="map" src="https://yandex.ru/map-widget/v1/?um=constructor%3Acb6609ff05c3a42d03b970bd4609d189c109a51326b040e7f5cdffd03fdaecb3&amp;source=constructor" width="500" height="400" frameborder="0"></iframe>
      <div class="map-ya-list">
        <div class="map-ya-item">
          <div class="map-ya-item-header">Адрес:</div>
          <div class="metro-mall">ТРЦ Саларис м. Саларьево</div>
          <span class="address">23-й километр Киевского шоссе, 1</span>
          <div class="working-hours-header">время работы:</div>
          <div class="working-hours">10:00 - 22:00</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.map-ya-box{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  box-sizing: content-box;
}
.map-ya-item-header{
  color: #9D9D9D;
  font-family: Montserrat;
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
  line-height: 140%;
  text-transform: uppercase;
}
.metro-mall, .address, .working-hours-header, .working-hours{
  color: #9D9D9D;
  font-family: Montserrat;
  font-size: 28px;
  font-style: normal;
  font-weight: 700;
  line-height: 131%;
}
.metro-mall{
  color: #DF5F26;
}
.map{
  padding-right: 7%;
}

@media (min-width: 1201px) {}

@media (min-width: 641px) and (max-width: 1200px) {


}
@media (min-width: 641px) and (max-width: 1068px) {
.map{
  padding-right: 0%;
  padding-bottom: 7%;
}

}

@media (max-width: 640px) {
  .map{
    padding-right: 0%;
  padding-bottom: 7%;
}
.map-ya-item{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.address{
  text-align: center;
}
}
@media (min-width: 376px) and (max-width: 425px){
  .map{
  padding-right: 0%;
  padding-bottom: 7%;
}
.map-ya-item{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.address{
  text-align: center;
}
}
@media (min-width: 320px) and (max-width: 375px){
  .map{
  padding-right: 0%;
  padding-bottom: 7%;
}
.map-ya-item{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.address{
  text-align: center;
}
}

</style>
