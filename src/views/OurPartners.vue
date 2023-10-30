<script setup>
import { ref } from "vue"
const RouterArr = ref([
  {
    name: 'О компании',
    to: '/About'
  },
  {
    name: 'Услуги',
    to: '/Services'
  },
  {
    name: 'Портфолио',
    to: ''
  },
  {
    name: 'Наши партнеры',
    to: '/our_partners'
  },
  {
    name: 'Вакансии',
    to: ''
  },
  {
    name: 'Контакты',
    to: ''
  },
])
</script>

<template>
<div class="wrappe">
    <header>
        <div class="up_menu">
        <div class="logo">
          <a href="/"><img src="/public/button/button_universoft.svg" alt=""></a>
        </div>
        <div class="nav">
          <nav>
            <ul>
              <li v-for="(item,i) in RouterArr" :key="i">
                <router-link :to="item?.to">{{ item?.name }}</router-link>
              </li>
            </ul>
          </nav>
        </div>
        <div class="contact_us">
          <div class="language">
            <img src="/public/button/RU.svg" />
          </div>
          <div class="number"><a href="tel:+998998999191"><button>+998 99 899 91 91</button></a></div>
        </div>
        </div>
        <div class="box">
        <div class="carusel">
            <span style="--i:1;">
                <a href="#"><img src="../../public/gallary/carusel/Davlocal.png" alt=""></a>
            </span>
            <span style="--i:2;">
                <a href="#"><img src="../../public/gallary/carusel/Uzguard.png" alt=""></a>
            </span>
            <span style="--i:3;">
                <a href="#"><img src="../../public/gallary/carusel/Davlocal.png" alt=""></a>
            </span>
            <span style="--i:4;">
                <a href="#"><img src="../../public/gallary/carusel/Uzguard.png" alt=""></a>
            </span>
            <span style="--i:5;">
                <a href="#"><img src="../../public/gallary/carusel/Uzguard.png" alt=""></a>
            </span>
            <span style="--i:6;">
                <a href="#"><img src="../../public/gallary/carusel/Davlocal.png" alt=""></a>
            </span>
            <span style="--i:7;">
                <a href="#"><img src="../../public/gallary/carusel/Uzguard.png" alt=""></a>
            </span>
            <span style="--i:7;">
                <a href="#"><img src="../../public/gallary/carusel/Uzguard.png" alt=""></a>
            </span>
        </div>
    </div>
    <div class="text_partners">
        <div class="info_partners">
        <img src="../../public/gallary/carusel/Наши_партнёры.svg" alt="">
        <img src="../../public/gallary/carusel/Сотрудничество.svg" alt="">
    </div>
    <div class="bg">
        <img class="line_bg" src="../../public/gallary/carusel/line-white.svg" alt="">
        <img src="../../public/gallary/carusel/line-black.png" alt="">
    </div>
    </div>
      </header>
</div>
</template>


<style>
header{
    background-color: #000;
}
.carusel{
   position: relative;
   width: 291px;
   height: 257px;
   transform-style: preserve-3d;
}
.carusel{
    animation: animate 45s linear infinite;
}
@keyframes animate{
    0%{
        transform: perspective(1000px) rotateY(0deg);
    }
    100%{
        transform: perspective(1000px) rotateY(360deg);
    }
}
.carusel span{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform-origin: center;
    transform-style: preserve-3d;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px); 
}
.carusel span img{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.info_partners :first-child {
    margin-bottom: 10px;
}
.bg :first-child{
    width: 1000px;
    height: 55px;
}
@import url("../assets/main.css");
</style>