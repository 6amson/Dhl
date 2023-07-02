<template>
  <div class="containerFooter">
    <div class="logo"><img :src="dhllogo" alt="Dhl logo" /></div>
    <ul class="firstListF">
      <li>Sitemap</li>
      <li>Help center</li>
      <li>Our divisions</li>
      <li>Industry sectors</li>
      <li>Company information</li>
      <li>Deutsche post DHL Group</li>
    </ul>
    <div class="finalfooterList">
      <ul class="secondListF">
        <li><img :src="instagram" alt="instagram Icon" /></li>
        <li><img :src="linkedin" alt="linkedin Icon" /></li>
        <li><img :src="twitter" alt="twitter Icon" /></li>
        <li><img :src="pinterest" alt="instagram Icon" /></li>
      </ul>

      <div class="thirdListF">
        <p>Contact Us</p>
        <p>
          <span class="material-symbols-sharp arrowEast"> north_east </span>
        </p>
      </div>
    </div>
  </div>
  <div class="footerfinal">2022 &copy; - all rights reserved.</div>
</template>

<script>
import dhllogo from "@/assets/dhllogo.svg";
import instagram from "../assets/instagram.svg";
import pinterest from "../assets/pinterest.svg";
import twitter from "../assets/twitter.svg";
import linkedin from "../assets/linkedin.svg";

export default {
  name: "FooterR",
  props: {},
  data() {
    return {
      instagram: instagram,
      dhllogo: dhllogo,
      pinterest: pinterest,
      twitter: twitter,
      linkedin: linkedin,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "@/styles/global.scss";
@import "@/styles/footer.scss";
</style>