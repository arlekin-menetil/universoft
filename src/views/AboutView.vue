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
      <a href="#"><img src="/public/button/button_universoft.svg" alt=""></a>
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
    <video muted loop autoplay plays-inline class="header_video">
      <source src="/public/bg/bgvideo.mp4" />
    </video>
    <div class="text_info">
    <img src="/public/button/innovation.svg" class="w-[1140px] h-[140px]" />
    <p>Мы считаем, что лучше тратить больше времени на наших клиентов, чем на себя
      Тем не<br> менее, пожалуйста, не стесняйтесь подать заявку</p>
    <a href="#"><button>Получить консультацию</button></a>
  </div>
  </header>
</div>
</template>


<style>
@import url("../assets/main.css");
</style>