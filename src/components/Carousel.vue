<template>
  <div>
    <b-carousel
      id="carousel-1"
      fade
      v-model="slide"
      :interval="2000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="280"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://picsum.photos/1024/480/?image=52"
        style="width:100%; height: 400px !important;"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54" style="width:100%; height: 400px !important;">
        <h1>Hello world!</h1>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58" style="width:100%; height: 400px !important;"></b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide style="width:100%; height: 400px !important;">
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://picsum.photos/1024/480/?image=55"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>

      <!-- Slide with blank fluid image to maintain slide aspect ratio -->
      <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image" style="width:100%; height: 400px !important;">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
          a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
        </p>
      </b-carousel-slide>
    </b-carousel>

    <div class="d-flex justify-content-around" style="font-size: 4rem;">
        <div>
          <b-icon icon="telephone-fill" class="border border-info rounded p-2" variant="info">
          </b-icon>
          <p style="font-size: 1rem;">Asesoria</p>
        </div>
        <div>
          <b-icon icon="sun" class="border border-info rounded p-2" variant="info">
          </b-icon>
          <p style="font-size: 1rem;">Beneficios</p>
        </div>
        <div>
          <b-icon icon="display" class="border border-info rounded p-2" variant="info">
          </b-icon>
          <p style="font-size: 1rem;">Como funciona?</p>
        </div>
        <div>
          <b-icon icon="gem" class="border border-info rounded p-2" variant="info">
          </b-icon>
          <p style="font-size: 1rem;">Precios</p>
        </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }
</script>