<template>
  <div class="caroussel">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="grey"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide
        text=""
        img-src="https://previews.123rf.com/images/vectorshowstudio/vectorshowstudio1702/vectorshowstudio170200582/71423773-divertidos-dibujos-animados-perros-personajes-diferentes-panes-ilustración-.jpg"
      >
      </b-carousel-slide>

      <b-carousel-slide
        img-src="https://img.freepik.com/vector-gratis/grupo-razas-perros-caza_81894-3809.jpg?w=1380"
      >
      </b-carousel-slide>

      <b-carousel-slide
        img-src="https://static7.depositphotos.com/1007989/773/i/950/depositphotos_7733780-stock-photo-dog-and-cat.jpg"
      ></b-carousel-slide>

      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://img.freepik.com/vector-gratis/conjunto-ilustracion-dibujos-animados-perros-divertidos_29190-141.jpg?w=1060"
            alt="image slot"
          />
        </template>
      </b-carousel-slide>

    </b-carousel>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>

<style lang="scss">

</style>
