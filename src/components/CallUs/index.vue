<template>
  <div class="call_us_container">
      <div class="container">
          <div class="first" v-scroll-reveal.reset = "{delay:200, scarle: 2}">
              <h1>Hungry ?</h1>
          </div>
          <div class="second">
            <app-anim></app-anim>
          </div>
          <div class="third" v-scroll-reveal.reset = "{delay:1000, scarle: 2}">
              <span>Give us a call </span>
              <span> 555-55-55</span>
          </div>
      </div>
  </div>
</template>

<script>
import Anim from './anim'
export default {
components:{
    appAnim: Anim
}
}
</script>

<style>

</style>