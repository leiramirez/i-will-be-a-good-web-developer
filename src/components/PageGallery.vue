<template>
  <div id="gallery">
    <h1 id="event-title">Upcoming Events</h1>
    <img @click="movePrev" v-if="!first" src='../assets/img/left.png' id="prev" alt="Previous button">
    <img @click="moveNext" v-if="!last" src='../assets/img/right.png' id="next" alt="Next button">
    <div id="slider">
      <div class="slide" ref="inner" :style="innerStyles">
        <img v-for="img in imgs" :key="img.idx" :src="img.path" class="gallery-img" :alt="img.alt">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      imgs: [
        {path: require('../assets/img/event-1.jpg'), alt: 'Poster for Paws Out event in Makati City'},
        {path: require('../assets/img/event-2.png'), alt: 'Poster for Pawssion Camp event in Quezon City'},
        {path: require('../assets/img/event-3.jpg'), alt: 'Poster for Furtastic Summer Bazaar event in Cebu City'},
        {path: require('../assets/img/event-4.jpg'), alt: 'Poster for Pet Trade Show 2022 in Parañaque City'}, 
        {path: require('../assets/img/event-5.jpg'), alt: 'Poster for Pet Huddle event in Taguig City'}
      ],
      innerStyles: {},
      step: 0,
      counter: 0,
      first: true,
      last: false
    }
  },
  methods: {
    setStep: function() {
      const innerWidth = this.$refs.inner.scrollWidth;
      const totalImgs = this.imgs.length;
      this.step = innerWidth / totalImgs
    },
    moveNext: function() {
      this.counter++;
      this.innerStyles = { transform: `translateX(-${this.step*this.counter}px)` }
      if(this.counter >= 1) {
        this.first = false;
      }
      if(this.counter >= this.imgs.length-2) {
        this.last = true;
      }
    },
    movePrev: function() {
      this.counter--;
      this.innerStyles = { transform: `translateX(-${this.step*this.counter}px)` }
      if(this.counter < 1) {
        this.first = true;
      }
      if(this.counter < this.imgs.length-2) {
        this.last = false;
      }
    }
  },
  mounted: function() {
    this.setStep();
  }
}
</script>

<style>
  @import '../assets/styles/gallery.css';
</style>
