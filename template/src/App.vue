<template>
  <div id="app">
    {{#router}}
    <Header/>
    <Nav/>
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
import AppHeader from './components/AppHeader'
import AppNav from './components/AppNav'
import AppBanner from './components/AppBanner'
import AppFooter from './components/AppFooter'
{{else}}
import HelloWorld from './components/HelloWorld'
{{/router}}

export default {
  name: 'App',
  components: {
    {{#router}}
    AppHeader,
    AppNav,
    AppBanner,
    AppFooter,
    {{else}}
    HelloWorld
    {{/router}}
  }
}
</script>

<style></style>
