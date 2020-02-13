<template>
  <header>
    <div class="container clear">
      <div class="logo"><img :src="logoIcon" alt="logo" /></div>
      <div class="nav">
        <img
          :src="menuIcon"
          alt="menu"
          @click="showSidepanel = !showSidepanel"
        />
      </div>
      <md-drawer
        class="side-drawer"
        :md-active.sync="showSidepanel"
        :md-right="true"
      />
    </div>
  </header>
</template>

<script>
import Logo from "../../assets/images/logo.png";
import Menu from "../../assets/images/menu.png";
export default {
  data() {
    return {
      logoIcon: Logo,
      menuIcon: Menu,
      showSidepanel: false
    };
  }
};
</script>

<style></style>
