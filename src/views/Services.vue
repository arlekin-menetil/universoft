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
          <source src="/public/bg/bgservice.mp4" />
        </video>
      </header>
</div>
</template>


<style>
header{
    background-color: rgba(0, 0, 0, 0.8);
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