<template>
  <div id="app">
    {{#router}}
    <router-view/>
    {{else}}
    <Header/>
    <Nav/>>
    <Banner/>
    <Footer/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import Header from './components/Header'
import Nav from './components/Nav'
import Banner from './components/Banner'
import Footer from './components/Footer'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    Header
    Nav
    Banner
    Footer
  }{{/router}}
}
</script>

<style></style>
