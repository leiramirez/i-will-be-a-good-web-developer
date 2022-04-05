<template>
  <div id="form">
    <div id="contact">
      <h1>Got any questions?</h1>
      <p>Send us a message, and we'll be happy to assist you!</p>
    </div>
    <div id="form-content">
      <form>
        <div id="form-fields">
          <input type="text" placeholder="First Name" required /><br>
          <input type="text" placeholder="Last Name" required /><br>
          <input type="email" placeholder="Email Address" required /><br>
          <input type="number" placeholder="Contact Number" required /><br>
          <input type="text" placeholder="Subject" required /><br>
          <textarea placeholder="Message"></textarea>
        </div>
        <div id="form-controls">
          <button id="send">Send</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>

<style>
  @import '../assets/styles/form.css';
</style>
