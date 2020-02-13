<template>
  <div class="anim_container">
    <div
      class="icon icon_phone"
      v-scroll-reveal.reset="{ delay: 300, scarle: 2 }"
    ></div>
    <div class="plus one" v-scroll-reveal.reset="{ delay: 450, scarle: 2 }">
      +
    </div>
    <div
      class="icon icon_delivery"
      v-scroll-reveal.reset="{ delay: 600, scarle: 2 }"
    ></div>
    <div class="equals one" v-scroll-reveal.reset="{ delay: 750, scarle: 2 }">
      =
    </div>
    <div
      class="icon icon_pizza"
      v-scroll-reveal.reset="{ delay: 900, scarle: 2 }"
    ></div>
  </div>
</template>

<script>
//import Velocity from 'velocity-animate'
export default {};
</script>

<style>
.anim_container {
  position: relative;
  height: 200px;
}
.icon {
  background-size: cover !important;
  position: absolute;
}
.plus {
  position: absolute;
  font-size: 160px;
  color: #ffffff;
  top: 90px;
  left: 310px;
}
.icon_phone {
  background: url("../../assets/images/icons/icon-phone.png");
  width: 130px;
  height: 130px;
  top: 30px;
  left: 100px;
}
.icon_delivery {
  background: url("../../assets/images/icons/icon-delivery.png");
  width: 200px;
  height: 200px;
  left: 480px;
}
.equals {
  position: absolute;
  font-size: 160px;
  color: #ffffff;
  top: 90px;
  left: 750px;
}
.icon_pizza {
  background: url("../../assets/images/icons/icon-pizza.png");
  width: 200px;
  height: 200px;
  left: 900px;
}
</style>
