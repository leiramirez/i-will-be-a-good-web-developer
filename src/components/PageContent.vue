<template>
  <div>
    <div class="container-1">
      <div id="text-1">
        <h1>Pet Care Made Easier</h1>
        <p>Paws Connect brings you closer to everything you need to care for your furry friend.</p>
      </div>
      <div id="img-1">
        <img src='../assets/img/mobile.png' class="img-size" alt="A mobile phone and a tablet with a paw print on their screens">
      </div>
    </div>
    <div class="container-2">
      <div id="text-2">
        <h1>The Nearest Services At Your Fingertips</h1>
        <p>From veterinary clinics to pet-friendly establishments, Paws Connect shows you all nearby available pet services for your convenience.</p>
      </div>
      <div id="box-venue">
        <ul id="list-venues">
          <li id="venues" v-for="venue in venues" :key="venue.id">
            <img :src="venue.img" :alt="venue.alt">
            <h3>{{ venue.name }}</h3>
          </li>
        </ul>
      </div>
      <button id="browse">Start Browsing</button>
    </div>
    <div class="container-1">
      <div class="box-content" id="review">
        <div id="text-3">
          <h1>For Pet Owners, By Pet Owners</h1>
          <p>Visited any of the establishments listed? Leave a review, so other owners can see your feedback!</p>
        </div>
        <div id="img-2">
          <img src='../assets/img/review.png' class="img-size" alt="A pencil and a feedback form with a smiling face and 4 stars">
        </div>
      </div>
      <div class="box-content" id="event">
        <div id="img-3">
          <img src='../assets/img/event.png' class="img-size" alt="A calendar with a paw print enclosed in a heart">
        </div>
        <div id="text-4">
          <h1>Join the Local Pet Community</h1>
          <p>Interested in connecting with other pets and pet owners? Check out upcoming events and bazaars you can attend!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      venues: [
        {name: 'Veterinary Clinics', img: require('../assets/img/vet.png'), alt: 'A veterinarian with a cat'}, 
        {name: 'Grooming Salons', img: require('../assets/img/grooming.png'), alt: 'A grooming brush for animals'},
        {name: 'Daycare Centers', img: require('../assets/img/daycare.png'), alt: 'A building with a signage of a dog and a cat enclosed in a heart'},
        {name: 'Pet-Friendly Establishments', img: require('../assets/img/pet-friendly.png'), alt: 'A paw print with a check mark'}
      ]
    }
  }
}
</script>

<style scoped>
  @import '../assets/styles/content.css';
</style>
