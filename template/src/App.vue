<template>
  <div id="app">
    {{#router}}
    <Header/>
    <Nav/>>
    <Banner/>
    <router-view/>
    <Footer/>
    {{else}}
    <HelloWorld/>
    {{/router}}
  </div>
</template>

<script>
{{#router}}
import Header from './components/Header'
import Nav from './components/Nav'
import Banner from './components/Banner'
import Footer from './components/Footer'
{{else}}
import HelloWorld from './components/HelloWorld'
{{/router}}

export default {
  name: 'App',
  components: {
    {{#router}}
    Header
    Nav
    Banner
    Footer
    {{else}}
    HelloWorld
  }{{/router}}
}
</script>

<style></style>
