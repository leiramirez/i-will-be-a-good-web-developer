<template>
  <div id="site">
    <page-header></page-header>
    <page-content></page-content>
    <div class="space"></div>
    <page-gallery></page-gallery>
    <div class="space"></div>
    <page-form></page-form>
    <page-footer></page-footer>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue'
import PageContent from './components/PageContent.vue'
import PageGallery from './components/PageGallery.vue'
import PageForm from './components/PageForm.vue'
import PageFooter from './components/PageFooter.vue'

export default {
  components: {
    'page-header': PageHeader,
    'page-content': PageContent,
    'page-gallery': PageGallery,
    'page-form': PageForm,
    'page-footer': PageFooter
  },
  data () {
    return {

    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');

  body {
    margin: 0;
    font-family: 'Roboto', sans-serif;
  }

  .space {
    background: #F2E8CF;
    max-width: 100%;
    min-height: 75px;
  }
</style>
