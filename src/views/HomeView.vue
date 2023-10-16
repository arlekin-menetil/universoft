<script setup>
import { ref } from "vue"
const RouterArr = ref([
  {
    name: 'О компании',
    to: '/About'
  },
  {
    name: 'Услуги',
    to: ''
  },
  {
    name: 'Портфолио',
    to: ''
  },
  {
    name: 'Наши партнеры',
    to: ''
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
<div class="wrapper">
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
  <main>
    <div class="company_work">
    <img src="/public/gallary/druk_text/company_work.svg">
  </div>
  <div class="our_client">
    <img src="/public/gallary/client/our1.svg" alt="">
    <img src="/public/gallary/client/our2.svg" alt="">
  </div>
  <div class="company">
    <div class="earth">
      <video muted loop autoplay plays-inline>
        <source src="/public/gallary/video/earth.mp4">
      </video>
    </div>
    <div class="about_company">
      <img src="/public/gallary/druk_text/about_company.svg" alt="">
      <p>Universoft-IT является ведущей компанией в области информационных технологий, специализирующейся на разработке инновационного программного обеспечения <br> и предоставлении широкого спектра услуг IT-консалтинга. Мы являемся надежным и непрерывно растущим партнером для клиентов во всем мире.</p>
    <img src="../../public/gallary/druk_text/our_client.svg" alt="">
    </div>
  </div>
  <div class="infiniti_earth">
  <div class="video_earth">
    <video muted loop autoplay plays-inline class="big_earth">
      <source src="/gallary/video/big_earth.webm" />
    </video>
  </div>
</div>
<div class="service">
  <div class="atom">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/atom.mp4">
    </video>
    <img src="../../public/gallary/druk_text/Что_мы.svg" />
    <p>Universoft-IT является ведущей компанией в области информационных технологий, <br> специализирующейся на разработке инновационного программного обеспечения </p>
  </div>
  <div class="servises">
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/Sait.webm">
    </video>
    <img src="../../public/gallary/servise/Разработкасайтов.svg" alt="">
    <p>Качественный сайт – это основа продвижения <br> Вашего бизнеса в интернете.</p>
  </div>
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/SMI.webm">
    </video>
    <img src="../../public/gallary/servise/РекламавСМИ.svg" alt="">
    <p>Предлагаем разнообразную рекламу на портале <br> Kun.uz - от публикации в Telegram до мероприятий</p>
  </div>
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/AI.webm">
    </video>
    <img src="../../public/gallary/servise/РазработкаAI.svg" alt="">
    <p>Качественный сайт – это основа продвижения <br> Вашего бизнеса в интернете.</p>
  </div>
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/SEO.webm">
    </video>
    <img src="../../public/gallary/servise/Seoпродвижение.svg" alt="">
    <p>Продвижение сайта в топ 10 Яндекса и Google <br> - будущие клиенты саAми найдут вас</p>
  </div>
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/AI.webm">
    </video>
     <img src="../../public/gallary/servise/CRM.svg" alt="">
     <p>CRM- и ERP-системы предназначены для <br> автоматизации и управления внутренними <br> рабочими процессами компании.</p>
  </div>
  <div class="serve">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/Sait.webm">
    </video>
    <img src="../../public/gallary/servise/Mobileapps.svg" alt="">
    <p>Мобильные приложения – необходимость для <br> оперативной реакции на изменения в любых сферах <br>
      и получения своевременной информации</p>
  </div>
</div>
</div>
<div class="line">
  <div class="line_image">
  <img src="/bg/line.svg" />
</div>
</div>
<div class="our_work">
<div class="text_potfolo">
  <div class="message">
    <video muted loop autoplay plays-inline>
      <source src="../../public/gallary/video/message.mp4">
    </video>
    <img src="../../public/gallary/druk_text/Впечатляющее.svg" />
  </div>
</div>
<div class="universoft_portfolio">
  <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item.svg" /></a></div>
  <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (1).svg" /></a></div>
  <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (2).svg" /></a></div>
  <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (3).svg" /></a></div>
</div>
</div>
<div class="message">
  <video muted loop autoplay plays-inline>
    <source src="../../public/gallary/video/message.mp4">
  </video>
  <img src="../../public/gallary/druk_text/Наши_продукты.svg" />
</div>
<div class="universoft_work">
  <div class="univework">
    <div class="uzgard">
      <img src="../../public/gallary/logo/uzgard.png" />
      <p>Ключевые носители UzGuard — линейка USB-токенов и <br> смарт-карт узбекского производства для подписания  документов ЭЦП и строгой двухфакторной <br> аутентификации на настольных и мобильных <br> устройствах. Продукты линейки являются <br> полнофункциональными аппаратными СКЗИ.</p>
      <a href=""><button>Перейти на сайт</button></a>
    </div>
    <div class="siema">
      <img src="../../public/gallary/logo/siyema.png" />
      <p>25 апреля 2019 года ООО «Авесто Групп» <br> заключила инвестиционное соглашение с<br> правительством Республики Таджикистан о<br> строительстве и вводе в эксплуатацию<br> предприятия по производству прохладительных<br> и спиртных напитков «Сиёма» в городе Душанбе.</p>
      <a href=""><button>Перейти на сайт</button></a>
    </div>
    <div class="dc">
      <img src="../../public/gallary/logo/dc.png" />
      <p>Переводы из России<br>
        в Таджикистан
        Выберите удобный способ<br> перевода
        из России на карты Dushanbe City</p>
      <a href=""><button>Перейти на сайт</button></a>
    </div>
  </div>
  <div class="logo_company">
    <img src="../../public/gallary/logo/logo-univer.png" />
  </div>
</div>
  </main>
</div>
</template>

<style>
.text_info a{
  color: #82F7FF;
  box-shadow: -2px 1px 15px 2px #82F7FF inset;
};
.atom{
box-shadow: -6px -41px 100px 57px rgba(34, 60, 80, 0.6);
};
.univework a{
  color: #82F7FF;
  box-shadow: -2px 1px 15px 2px #82F7FF inset;
};
@import url("../assets/main.css");
</style>