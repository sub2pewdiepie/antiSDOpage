<template>
  <div id="app">
    <header class="app-header">
      <span class="nav-link" @click="goToSlide(0)">Описание</span>
      <span class="nav-link" @click="goToSlide(1)">Видеодемонстрация</span>
      <span class="nav-link" @click="goToSlide(2)">Инструкция</span>
      <span class="nav-link" @click="goToSlide(3)">Контакты</span>
    </header>

    <Swiper
      ref="mySwiper"
      direction="vertical"
      :modules="[Navigation, Pagination, Keyboard, Mousewheel]"
      :slides-per-view="1"
      :space-between="30"
      :pagination="{ clickable: true }"
      :keyboard="{ enabled: true }"
      :mousewheel="true"
      class="my-swiper"
      @swiper="onSwiper"
    >
      <SwiperSlide>
        <DescriptionPage />
      </SwiperSlide>
      <SwiperSlide>
        <div class="video-slide">
          <h2>Видеодемонстрация</h2>
          <video src="./assets/demo.mp4" controls></video>
        </div>
      </SwiperSlide>
      <SwiperSlide>
        <InstructionPage />
      </SwiperSlide>
      <SwiperSlide>
        <ContactSection />
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<script>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
// Импорт модулей Swiper
import { Navigation, Pagination, Keyboard, Mousewheel } from 'swiper/modules'

// Импорт стилей Swiper
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

import DescriptionPage from './components/DescriptionPage.vue'
import ContactSection from './components/ContactSection.vue'
import InstructionPage from './components/InstructionPage.vue'

export default {
  name: 'App',
  components: {
    Swiper,
    SwiperSlide,
    DescriptionPage,
    ContactSection,
    InstructionPage,
  },
  setup() {
    const swiperInstance = ref(null)

    const onSwiper = (swiper) => {
      swiperInstance.value = swiper
    }

    const goToSlide = (index) => {
      if (swiperInstance.value) {
        swiperInstance.value.slideTo(index, 800)
      }
    }

    return {
      onSwiper,
      goToSlide,
      Navigation,
      Pagination,
      Keyboard,
      Mousewheel,
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

.app-header {
  background-color: #2563eb;
  color: white;
  padding: 1.25rem 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  flex-shrink: 0;
}

.nav-link {
  cursor: pointer;
  font-size: 1rem;
}

.nav-link:hover {
  text-decoration: underline;
}

.video-slide {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  box-sizing: border-box;
  padding: 1rem;
}

.video-slide h2 {
  margin-bottom: 1rem;
}

.video-slide video {
  max-width: 90%;
  max-height: 80%;
  border-radius: 0.5rem;
  outline: none;
}
.my-swiper {
  width: 100%;
  position: relative;
  min-height: 0;
}
.swiper {
  height: 100%;
}
.swiper-pagination-vertical.swiper-pagination-bullets,
.swiper-vertical > .swiper-pagination-bullets {
  right: 10px;
  top: 50%;
  transform: translateY(-50%);
}

.swiper-slide {
  user-select: text;
}
</style>
