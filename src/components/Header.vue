<template>
  <div class="containerHeader">
    <div class="logo"><img :src="dhllogo" alt="Dhl logo" /></div>
    <ul class="firstList">
      <li>Products & Services</li>
      <li>Industry  Sectors</li>
      <li>About Us</li>
    </ul>
    <ul class="secondList">
      <li>En</li>
      <li><span class="material-symbols-sharp search"> search </span></li>
    </ul>
    <div class="Menu">Menu</div>
  </div>
</template>

<script>
import dhllogo from "@/assets/dhllogo.svg";

export default {
  name: "HeadeR",
  props: {},
  data() {
    return {
      dhllogo: dhllogo,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "@/styles/global.scss";
@import "@/styles/header.scss";
</style>
