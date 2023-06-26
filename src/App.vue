<template>
  <div id="app">
    <PageHeader/>
    <MainPage/>
    <PageFooter/>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue';
import MainPage from './components/MainPage.vue';
import PageFooter from './components/PageFooter.vue';

export default {
  name: 'App',
  components: {
    PageHeader,
    MainPage,
    PageFooter
  }
}
</script>

<style>
@import './styles/global.css';

/* Your existing styles */

</style>
