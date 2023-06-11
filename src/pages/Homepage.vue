<template>
  <div class="Container">
    <div class="mainContainer">
      <div class="headerDIv"><Header /></div>
      <div class="subMainh1">
        <h1>logistics for the connected age</h1>
      </div>
      <div class="subMainContainer">
        <input
          type="text"
          v-model.number="age"
          placeholder="Tracking number"
          class="subMainInput"
        />
        <div class="subMainSubmit"><p>Ok</p></div>
      </div>
      <div class="gridMenu">
        <div class="firstGrid">
          <div class="firstGridDiv1">
            <p>Portal login</p>
            <p>
              <span class="material-symbols-sharp arrowEast"> north_east </span>
            </p>
          </div>
          <div class="firstGridDiv2">
            <p>220</p>
            <p>Countries and regions</p>
          </div>
        </div>

        <div class="secondGrid">
          <div class="secondGridDiv1">
            <p>DHL remove for business</p>
            <p>
              <span class="material-symbols-sharp arrowEast"> north_east </span>
            </p>
          </div>
        </div>

        <div class="thirdGrid">
          <div class="thirdGridDiv">
            <div class="thirdGridDiv1">
              <p>Ship now</p>
            </div>
            <div class="thirdGridDiv2">
              <p>Get A Quote</p>
            </div>
          </div>
        </div>
      </div>

      <div class="statDiv">
          <div class="statItem firstStatDiv">
              <p>120k</p>
              <p>Cities</p>
          </div>

          <div class="statItem secondStatDiv">
              <p>84k</p>
              <p>Offices</p>
          </div>

          <div class="statItem thirdStatDiv">
              <p>34k</p>
              <p>Delivery Vehicles</p>
          </div>
      </div>

      <div class="gridMenu2">
          <div class="firstGridMenu2">
              <p>Rail Freight</p>
          </div>
          <div class="secondGridMenu2">
              <p>Document & Parcel</p>
          </div>
          <div class="thirdGridMenu2">
              <p>Road Freight</p>
          </div>
          <div class="fourthGridMenu2">
              <p>Air Freight</p>
          </div>
          <div class="fifthGridMenu2">
              <p>Discover</p>
          </div>
          <div class="sixthGridMenu2">
              <p>Ocean Freight</p>
          </div>
          <div class="seventhGridMenu2">
              <p>Shipping Service</p>
          </div>
      </div>
    </div>

    <div class="priContainer">
        
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";

export default {
  name: "HomePage",
  components: {
    Header,
  },
  data() {
    return {
      age: "",
    };
  },
  watch: {
    age() {
      console.log("Age:", this.age);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/global.scss";
@import "@/styles/header.scss";
@import "@/styles/homepage.scss";
</style>