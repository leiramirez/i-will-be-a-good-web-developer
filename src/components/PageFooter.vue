<template>
  <footer>
    <div id="text">
      <h3>PAWS CONNECT</h3>
      <p>Paws Connect is an initiative to connect pet owners with great services and businesses.</p>
    </div>
    <div class="sections">
      <h4>About Us</h4>
      <ul class="sections-list">
        <li class="sections-text" v-for="x in about" :key="x"><a class="f-link" href="#">{{ x }}</a></li>
      </ul>
    </div>
    <div class="sections">
      <h4>Join Us</h4>
      <ul class="sections-list">
        <li class="sections-text" v-for="x in join" :key="x"><a class="f-link" href="#">{{ x }}</a></li>
      </ul>
    </div>
    <div class="sections">
      <h4>Contact Us</h4>
      <ul class="sections-list">
        <li class="sections-text" v-for="x in contact" :key="x"><a class="f-link" href="#">{{ x }}</a></li>
      </ul>
    </div>
  </footer>
</template>
 
<script>
export default {
  data () {
    return {
      about: ['Our Story', 'The Team', 'FAQs'],
      join: ['Volunteer', 'Partner', 'Feature'],
      contact: ['hey@pawsconnect.com', 'Facebook', 'Instagram']
    }
  },
  methods: {

  }
}
</script>

<style scoped>
  @import '../assets/styles/footer.css';
</style>
