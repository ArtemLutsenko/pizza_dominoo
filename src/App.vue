<template>
  <div>
    <app-header></app-header>
    <div>
      <app-featured />
    </div>
    <app-menu></app-menu>
    <app-call-us></app-call-us>
    <app-newsletter></app-newsletter>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './components/Header-Footer/Header'
import Footer from './components/Header-Footer/Footer'
import Featured from './components/Featured/index'
import Menu from './components/Menu/index'
import CallUs from './components/CallUs/index'
import NewsLetter from './components/Newsletter'
export default {
  components:{
    appHeader: Header,
    appFooter: Footer,
    appFeatured: Featured,
    appMenu: Menu,
    appCallUs: CallUs,
    appNewsletter: NewsLetter
  }
}
</script>

<style>
@import './assets/style.css';
</style>