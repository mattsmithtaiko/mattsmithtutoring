<template>
  <v-container fluid fill-height class="splash" style="max-height: 100vh">
    <v-layout justify-center align-center column pa-5>
      <v-container
        elevation-24
        class="mb-16"
        style="background: rgba(96, 125, 139, 0.9)"
      >
        <div
          class="text-h1 font-weight-black text-center primary--text text--lighten-1"
          style="font-size: 5rem !important"
        >
          THE STRUGGLE IS REAL
        </div>
        <div class="text-h1 font-weight-black text-center mb-3 accent--text">
          BUT YOU CAN DO IT!
        </div>
        <div class="text-h4 font-weight-bold text-center white--text px-16">
          Learn to embrace challenge, build confidence, overcome fear, and
          sharpen the mind&mdash;all while improving your grades.
        </div>
      </v-container>
      <v-container>
        <div
          class="elevation-12 mx-8 px-8 py-4"
          style="background: rgba(96, 125, 139, 0.7)"
        >
          <div class="mt-n12 ml-n8" style="position: absolute; fill: #607d8b">
            <svg
              width="12rem"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              version="1.1"
              viewBox="0 0 100 100"
              xml:space="preserve"
            >
              <path
                d="M94.8,57.3c-1.3-8.7-8.7-14.9-17.1-15.3c2.1-7.8,7.2-10.9,13.4-12.7c0.6-0.2,0.5-0.8,0.5-0.8l-1-6.2c0,0-0.1-0.5-0.9-0.4  c-21.4,2.4-35.9,18.7-33.2,38.5C59,74.1,69.7,79.4,79.6,78C89.5,76.4,96.3,67.2,94.8,57.3L94.8,57.3z M26.5,42  c2-7.8,7.3-10.9,13.4-12.7c0.6-0.2,0.5-0.8,0.5-0.8l-0.9-6.2c0,0-0.1-0.5-0.9-0.4C17.2,24.2,2.8,40.5,5.3,60.3  C7.9,74.1,18.7,79.4,28.5,78c9.9-1.6,16.7-10.8,15.1-20.7C42.3,48.5,35,42.3,26.5,42z"
              ></path>
            </svg>
          </div>
          <v-carousel height="10rem" show-arrows-on-hover hide-delimiters cycle>
            <v-carousel-item
              class="text-h4 font-weight-bold white--text px-24"
              v-for="testimonial in testimonials"
              :key="testimonial.text"
              transition="fade-transition"
              reverse-transition="fade-transition"
            >
              <div class="white--text">
                <div style="position: absolute">
                  {{ testimonial.text }}
                </div>
                <div
                  class="d-flex align-end justify-end"
                  style="position: absolute; width: 100%; height: 100%"
                >
                  - {{ testimonial.attribution }}
                </div>
              </div>
            </v-carousel-item>
          </v-carousel>
        </div>
      </v-container>
      <v-btn fab class="mt-5 accent" @click="downArrowClick">
        <v-icon large color="white">mdi-chevron-down</v-icon>
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'Splash',
  data: () => ({
    testimonials: [
      {
        text:
          'Learn to embrace the challenge, build confidence, overcome the fear, and sharpen the mind all while improving your grades.',
        attribution: 'M. Smith'
      },
      {
        text: 'Some other testimonial.',
        attribution: 'I. Haveareallyfrickinlongname'
      }
    ]
  }),
  methods: {
    downArrowClick: function () {
      window.scrollBy({
        top: window.innerHeight,
        behavior: 'smooth'
      })
    }
  }
}
</script>

<style scoped>
.splash {
  background: url('../assets/jeswin-thomas-hecib2an4T4-unsplash.jpg');
  background-size: cover;
  width: 100%;
  height: 100%;
}

.backing {
  opacity: 0.25;
}
</style>
