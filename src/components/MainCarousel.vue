<template>
  <q-carousel
    v-model="slide"
    transition-prev="jump-right"
    transition-next="jump-left"
    swipeable
    animated
    control-color="green-10"
    prev-icon="arrow_left"
    next-icon="arrow_right"
    navigation-icon="radio_button_unchecked"
    navigation
    padding
    arrows
    height="45vh"
    class="bg-green-5 text-green-10 shadow-1 rounded-borders"
  >
    <q-carousel-slide
      name="main"
      img-src="/imgs/carousel/screen01.png"
      class="column no-wrap flex-center"
    >
      <div class="q-mt-md flex-center text-center">
        <div class="absolute-bottom custom-caption">
          <q-icon name="style" size="56px" />
          <div class="slide-title-h2">{{ title }}</div>
          <div class="slide-subtitle">{{ caption }}</div>
        </div>
      </div>
    </q-carousel-slide>

    <q-carousel-slide
      name="greet"
      img-src="/imgs/carousel/screen02.png"
      class="column no-wrap flex-center text-center"
    >
      <div class="q-mt-md flex-center text-center">
        <div class="absolute-bottom custom-caption">
          <q-icon name="style" size="56px" />
          <div class="slide-title-h2">{{ title }}</div>
          <div class="slide-subtitle">{{ caption }}</div>
        </div>
      </div>
    </q-carousel-slide>

    <q-carousel-slide
      name="about"
      img-src="/imgs/carousel/screen03.png"
      class="column no-wrap flex-center text-center"
    >
      <div class="q-mt-md flex-center text-center">
        <div class="absolute-bottom custom-caption">
          <q-icon name="style" size="56px" />
          <div class="slide-title-h2">{{ title }}</div>
          <div class="slide-subtitle">{{ caption }}</div>
        </div>
      </div>
    </q-carousel-slide>
  </q-carousel>
</template>

<script>
export default {
  name: 'MainCarousel',

  data() {
    return {
      slide: 'main',
      title: 'Slide 1',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
    return {
      slide: 'greet',
      title: 'Slide 2',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
    return {
      slide: 'about',
      title: 'Slide 2',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>