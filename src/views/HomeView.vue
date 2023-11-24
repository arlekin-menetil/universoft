<script setup>
import { computed, onMounted, ref } from "vue"
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
const btnShow = ref(true)
const screenSize = ref({ width: window.innerWidth, height: window.innerHeight });
const updateScreenSize = () => {
  screenSize.value = { width: window.innerWidth, height: window.innerHeight };
};

onMounted(()=>{
  window.addEventListener('resize', ()=>{
    updateScreenSize()
    if (screenSize.value.width>800) {
    btnShow.value = false
  } else {
    btnShow.value = true
  }
  });
  
})
</script>

<template>
  <div class="wrapper">
    <header class="header">
      <div class="up_menu" :class="btnShow ? 'up' : 'up_menu_show'" >
        <div class="base_logo">
          <div class="logo">
            <a href="#"><img src="/public/button/button_universoft.svg" alt=""></a>
          </div>
          <div class="manue_burger">
            <svg @click="btnShow = !btnShow" v-if="btnShow" width="19" height="19" viewBox="0 0 19 19" fill="none"
              xmlns="http://www.w3.org/2000/svg">
              <g clip-path="url(#clip0_377_593)">
                <path
                  d="M1.1875 4.75H17.8125C18.1274 4.75 18.4295 4.62489 18.6522 4.40219C18.8749 4.17949 19 3.87744 19 3.5625C19 3.24756 18.8749 2.94551 18.6522 2.72281C18.4295 2.50011 18.1274 2.375 17.8125 2.375H1.1875C0.872555 2.375 0.57051 2.50011 0.347811 2.72281C0.125111 2.94551 0 3.24756 0 3.5625C0 3.87744 0.125111 4.17949 0.347811 4.40219C0.57051 4.62489 0.872555 4.75 1.1875 4.75Z"
                  fill="#EBEBEB" />
                <path
                  d="M17.8122 6.33325H7.52051C7.20556 6.33325 6.90352 6.45836 6.68082 6.68106C6.45812 6.90376 6.33301 7.20581 6.33301 7.52075C6.33301 7.8357 6.45812 8.13774 6.68082 8.36044C6.90352 8.58314 7.20556 8.70825 7.52051 8.70825H17.8122C18.1271 8.70825 18.4292 8.58314 18.6519 8.36044C18.8746 8.13774 18.9997 7.8357 18.9997 7.52075C18.9997 7.20581 18.8746 6.90376 18.6519 6.68106C18.4292 6.45836 18.1271 6.33325 17.8122 6.33325Z"
                  fill="#EBEBEB" />
                <path
                  d="M17.8122 14.25H7.52051C7.20556 14.25 6.90352 14.3751 6.68082 14.5978C6.45812 14.8205 6.33301 15.1226 6.33301 15.4375C6.33301 15.7524 6.45812 16.0545 6.68082 16.2772C6.90352 16.4999 7.20556 16.625 7.52051 16.625H17.8122C18.1271 16.625 18.4292 16.4999 18.6519 16.2772C18.8746 16.0545 18.9997 15.7524 18.9997 15.4375C18.9997 15.1226 18.8746 14.8205 18.6519 14.5978C18.4292 14.3751 18.1271 14.25 17.8122 14.25Z"
                  fill="#EBEBEB" />
                <path
                  d="M17.8125 10.2917H1.1875C0.872555 10.2917 0.57051 10.4169 0.347811 10.6396C0.125111 10.8623 0 11.1643 0 11.4792C0 11.7942 0.125111 12.0962 0.347811 12.3189C0.57051 12.5416 0.872555 12.6667 1.1875 12.6667H17.8125C18.1274 12.6667 18.4295 12.5416 18.6522 12.3189C18.8749 12.0962 19 11.7942 19 11.4792C19 11.1643 18.8749 10.8623 18.6522 10.6396C18.4295 10.4169 18.1274 10.2917 17.8125 10.2917Z"
                  fill="#EBEBEB" />
              </g>
              <defs>
                <clipPath id="clip0_377_593">
                  <rect width="19" height="19" fill="white" />
                </clipPath>
              </defs>
            </svg>
            <svg @click="btnShow = !btnShow" v-if="!btnShow" width="28" height="29" viewBox="0 0 28 29" fill="none"
              xmlns="http://www.w3.org/2000/svg">
              <rect x="0.824219" y="1.12817" width="26.9258" height="26.9258" rx="13.4629" stroke="#82F7FF"
                stroke-width="0.5" />
              <path
                d="M18.6432 10.2346C18.5071 10.0984 18.3224 10.022 18.1299 10.022C17.9374 10.022 17.7527 10.0984 17.6166 10.2346L14.2868 13.5643L10.957 10.2346C10.8209 10.0984 10.6362 10.022 10.4437 10.022C10.2512 10.022 10.0665 10.0984 9.93036 10.2346C9.79424 10.3707 9.71777 10.5554 9.71777 10.7479C9.71777 10.9404 9.79424 11.1251 9.93036 11.2612L13.2601 14.591L9.93036 17.9208C9.79424 18.0569 9.71777 18.2416 9.71777 18.4341C9.71777 18.6266 9.79424 18.8113 9.93036 18.9474C10.0665 19.0836 10.2512 19.16 10.4437 19.16C10.6362 19.16 10.8209 19.0836 10.957 18.9474L14.2868 15.6177L17.6166 18.9474C17.7527 19.0836 17.9374 19.16 18.1299 19.16C18.3224 19.16 18.5071 19.0836 18.6432 18.9474C18.7794 18.8113 18.8558 18.6266 18.8558 18.4341C18.8558 18.2416 18.7794 18.0569 18.6432 17.9208L15.3135 14.591L18.6432 11.2612C18.7794 11.1251 18.8558 10.9404 18.8558 10.7479C18.8558 10.5554 18.7794 10.3707 18.6432 10.2346Z"
                fill="#82F7FF" />
            </svg>

          </div>
        </div>
        <div class="nav" v-if="!btnShow">
          <nav>
            <ul class="nav_ul">
              <li class="nav_li" v-for="(item, i) in RouterArr" :key="i">
                <router-link :to="item?.to">{{ item?.name }}</router-link>
              </li>
            </ul>
          </nav>
        </div>
        <div class="contact_us" v-if="!btnShow">
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
        <p class="inovatsiya_title">Инновации с Universoft-IT ваш путь {{ btnShow }}
          к лидерству в цифровой эпохе.</p>
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
          <video muted loop autoplay plays-inline >
            <source src="/public/gallary/video/earth.mp4">
          </video>
        </div>
        <div class="about_company">
          <img src="/public/gallary/druk_text/about_company.svg" alt="">
          <p>Universoft-IT является ведущей компанией в области информационных технологий, специализирующейся на
            разработке инновационного программного обеспечения <br> и предоставлении широкого спектра услуг
            IT-консалтинга. Мы являемся надежным и непрерывно растущим партнером для клиентов во всем мире.</p>
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
          <p>Universoft-IT является ведущей компанией в области информационных технологий, <br> специализирующейся на
            разработке инновационного программного обеспечения </p>
        </div>
        <div class="servises">
          <div class="servis">
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
          <div class="portfolio"><a href="#"><img  src="../../public/gallary/portfolio/Item.svg" /></a></div>
          <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (1).svg" /></a></div>
          <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (2).svg" /></a></div>
          <div class="portfolio"><a href="#"><img src="../../public/gallary/portfolio/Item (3).svg" /></a></div>
        </div>
      </div>
      <div class="message message_work">
        <video muted loop autoplay plays-inline>
          <source src="../../public/gallary/video/message.mp4">
        </video>
        <img src="../../public/gallary/druk_text/Наши_продукты.svg" />
      </div>
      <div class="universoft_work">
        <div class="univework">
          <div class="uzgard">
            <img src="../../public/gallary/logo/uzgard.png" />
            <p>Ключевые носители UzGuard — линейка USB-токенов и <br> смарт-карт узбекского производства для подписания
              документов ЭЦП и строгой двухфакторной <br> аутентификации на настольных и мобильных <br> устройствах.
              Продукты линейки являются <br> полнофункциональными аппаратными СКЗИ.</p>
            <a href=""><button>Перейти на сайт</button></a>
          </div>
          <div class="siema">
            <img src="../../public/gallary/logo/siyema.png" />
            <p>25 апреля 2019 года ООО «Авесто Групп» <br> заключила инвестиционное соглашение с<br> правительством
              Республики Таджикистан о<br> строительстве и вводе в эксплуатацию<br> предприятия по производству
              прохладительных<br> и спиртных напитков «Сиёма» в городе Душанбе.</p>
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
    <footer>
      <div class="footer_menu">
        <div class="footer_category">
          <div >
            <img src="../../public/gallary/druk_text/О_компании.svg" alt="">
          </div>
          <div>
            <p>Universoft-IT является ведущей компанией в области <br>
              информационных технологий, специализирующейся<br>
              на разработке инновационного программного<br>
              обеспечения и предоставлении широкого спектра<br>
              услуг IT-консалтинга.</p>
          </div>
          <div class="footer_icons">
            <a href="#"><img src="../../public/gallary/icons/youtube.png" alt=""></a>
            <a href="#"><img src="../../public/gallary/icons/telegramm.png" alt=""></a>
            <a href="#"><img src="../../public/gallary/icons/instagramm.png" alt=""></a>
          </div>
        </div>
        <div class="footer_category">
          <img src="../../public/gallary/druk_text/Услуги.svg" alt="">
          <ul>
            <li><a href="">Разработка сайтов</a></li>
            <li><a href="">Реклама в СМИ</a></li>
            <li><a href="">Разработка брендбуков</a></li>
            <li><a href="">Seo продвижение</a></li>
          </ul>
        </div>
        <div class="footer_category">
          <img src="../../public/gallary/druk_text/Полезные_ссылки.svg" alt="">
          <ul>
            <li><a href="">Разработка сайтов</a></li>
            <li><a href="">Реклама в СМИ</a></li>
            <li><a href="">Разработка брендбуков</a></li>
            <li><a href="">Seo продвижение</a></li>
          </ul>
        </div>
        <div class="footer_category">
          <img src="../../public/gallary/druk_text/Контактные_данные.svg" alt="">
          <ul>
            <li>г.Ташкент, ул.Тараса Щевченько 22,</li>
            <li><a href="">info@universoft.uz</a></li>
            <li><a href="tel:+998998999191">+998 99 899 91 91</a></li>
            <li>Пн. - Сб. 9:00 до 19:00</li>
          </ul>
        </div>
      </div>
      <div class="footer_copyright">
        <img src="../../public/gallary/line/Line.svg" alt="">
        <p>Копирование материалов сайта разрешается с ссылкой на сайт. <br>
          В противном случае копирование преследуется по закону</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
@import url("../assets/main.css");

.inovatsiya_title {
  font-size: 45px;
  font-weight: bold;
}

.portfolio>a > img{
  height: 100%!important;
}
.up_menu {
  display: flex;
  justify-content: space-around;
}

.manue_burger {
  cursor: pointer;
  display: none;
}

.serve {
  border: 1px solid #82F7FF;
}

.serve div:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: calc(100% + 4px);
  height: 100%;
  background: #fff;
}

.number {
  border-radius: 15px 15px 15px;
}

.text_info a {
  color: #82F7FF;
  box-shadow: -2px 1px 15px 2px #82F7FF inset;
}

.atom {
  box-shadow: -6px -41px 100px 57px rgba(34, 60, 80, 0.6);
}

.univework a {
  color: #82F7FF;
  box-shadow: -2px 1px 15px 2px #82F7FF inset;
}

.header_video {
  position: absolute;
  height: 100vh;
  z-index: -1;

}

.base_logo {
  width: fit-content;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

@media screen and (max-width: 800px) {
  .manue_burger {
    display: block;
  }

.big_earth{
  margin-left: 30vw;
  width: 50% !important;
  height: 50% !important;
}

  .up_menu {
    width: 100%;
    height: 100%;
    position: absolute;
    display: flex;
    align-items: start;
    top: 0;
    left: 0;
    z-index: 99;

    justify-content: space-between;
    padding: 50px 20px;
  }

  .base_logo {
    width: 100%;
  }

  .up_menu_show {
    position: fixed;
    
    background: linear-gradient(180deg, rgba(0, 0, 0, 0.50) 0%, rgba(22, 168, 211, 0.50) 105.43%);
    backdrop-filter: blur(25px);
  }

  .nav {
    width: 100%;
    position: absolute;
    top: 200px;
    left: 0;
    display: flex;
    justify-content: center;
    height: 100vh;
  }

  .nav_hide {
    display: none;
  }

  .nav_ul {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .nav_li {
    padding: 10px 0;

  }
.universoft_work{
  padding:  0 20px;
}
.message_work{
  padding:  0 20px;
}
  .logo {
    width: 100px;

  }

  .inovatsiya_title {
    font-size: 21px;
    font-weight: bold;
    letter-spacing: 0.05em;
  }
  .logo_company{
    display: none;
  }
  .contact_us {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 120px;
  }

  .language {
    width: 210px;
    height: 50px;
    display: flex;
    justify-content: center;
    border-radius: 14px;
    color: black;
    background-color: white;
  }
.servis{
  display: flex;
  flex-wrap: wrap;
  
}
  .about_company {
    padding-left: 20px;
    padding-right: 20px;
  }
}</style>