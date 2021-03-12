<template>
  <q-carousel
    v-model="slide"
    transition-prev="jump-right"
    transition-next="jump-left"
    swipeable
    animated
    control-color="white"
    prev-icon="arrow_left"
    next-icon="arrow_right"
    navigation-icon="radio_button_unchecked"
    navigation
    padding
    arrows
    height="50vh"
    class="bg-green-7 text-white shadow-1 rounded-borders"
  >
    <q-carousel-slide
      name="main"
      img-src="slide.back(value)"
      class="column no-wrap flex-center"
    >
      <q-icon name="style" size="56px" />
      <div class="q-mt-md text-center">
        {{ caption }}
      </div>
    </q-carousel-slide>

    <q-carousel-slide
      name="greet"
      img-src="slide.back(value)"
      class="column no-wrap flex-center"
    >
      <q-icon name="style" size="56px" />
      <div class="q-mt-md text-center">
        {{ caption }}
      </div>
    </q-carousel-slide>

    <q-carousel-slide
      name="about"
      img-src="slide.back(value)"
      class="column no-wrap flex-center"
    >
      <q-icon name="style" size="56px" />
      <div class="q-mt-md text-center">
        {{ caption }}
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
      back: '~/public/imgs/carousel/screen01.png',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
    return {
      slide: 'greet',
      back: '~/public/imgs/carousel/screen02.png',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
    return {
      slide: 'about',
      back: '~/public/imgs/carousel/screen03.png',
      caption:
        'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>