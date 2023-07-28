<script >

</script>

<template>

<div class="content-box">
<div id="slogan">
    <span>территория радости и веселья</span>
    
</div>
<div class="castle">
  <div class="ball ball-1"></div>
  <div class="ball ball-2"></div>
  <div class="ball ball-3"></div>
  <div class="ball ball-4"></div>
  <div class="ball ball-5"></div>
  <div class="ball ball-6"></div>
  <div class="ball ball-7"></div>
  <img src="../assets/slogan/zamok.svg" alt="Castle" class="castle-image" />
</div>
</div>
</template>

<style >
.content-box{
    height: 599px;
    position: relative;
    z-index: 1;
    margin-top: 10%;
}
#slogan span {
    position: relative;
    font-family: "PoetsenOne";
    font-size: 36px;
    color: #676190;
    padding-left: 20.5%;
    z-index: 99;
}
#slogan{
    margin-top: 50px;
}
@keyframes ballAnimation {
  0% {
    position: absolute;
    opacity: 1;
    top: 80%;
    left: 30%;
  }
  50% {
    opacity: 0.5;
    top: 80%;
    left: 85%;
  }
  100% {
    transform: translate(-600px, 0) rotate(720deg);
    opacity: 1;
  }
}

.castle {
  position: absolute;
  width: 600px;
  height: 400px;
  top: -5%;
  right: 20%;
}

.ball {
  position: absolute;
  width: 50px;
  height: 50px;
  background-repeat: no-repeat;
  background-size: contain;
}

.ball-1 {
    top: 110%;
    left: 10%;
    background-image: url(../assets/slogan/smail.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 85.006px;
    height: 87.909px;
}

.ball-2 {
    top: 60%;
    left: 95%;
    background-image: url(../assets/slogan/smail1.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 166.423px;
    height: 172.132px;
}

.ball-3 {
    top: 110%;
    left: 180%;
    background-image: url(../assets/slogan/smail2.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 89.534px;
    height: 92.581px;
}
.ball-4 {
    top: 38%;
    left: 101%;
    background-image: url(../assets/slogan/smail3.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 98.699px;
    height: 102.085px;
}
.ball-5 {
    top: 60%;
    left: 60%;
    background-image: url(../assets/slogan/smail4.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 69.006px;
    height: 69.037px;
}
.ball-6 {
    top: 140%;
    left: 150%;
    background-image: url(../assets/slogan/smail5.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 112.644px;
    height: 116.513px;
}
.ball-7 {
    top: 90%;
    left: 80%;
    background-image: url(../assets/slogan/smail6.svg);
    animation: ballAnimation 3s ease-in-out forwards;
    width: 82.994px;
    height: 85.81px;
}

@media (max-width: 640px) {

}
@media (min-width: 641px) and (max-width: 1200px) {
  .header{
    position: fixed;
    z-index: 9999;
    background-color: #fffffF !important;
    top: 0;
    width: 100%;
    justify-content: space-around !important;

  }
   .content-box{
    margin-top: 20%;
   }

}
@media (min-width: 1201px) {}
</style>