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
      <div class="subPriContainer">
        <div class="preFirstPriContainer">
          <p>Logistics</p>
          <p>Solutions</p>
        </div>
        <div @click="toggleElement" class="firstPriContainer">
          <div class="firstPriContainerDiv">
            <p>01</p>
            <p ref="moreTitle" class="moreTitle">Warehouse Solutions</p>
            <p>
              <span ref="moreArrow" class="material-symbols-sharp moreArrow">
                arrow_upward
              </span>
            </p>
          </div>
        </div>

        <div ref="moreBody" v-show="showElement" class="secondPriContainer">
          <div class="secondPriContainerDiv">
            <div class="secondPriContainerPara">
              <p>
                We have various warehouses across countries facilitating the
                storage of our clients packages. we understand the critical role
                that warehousing plays in the logistics process. Our spacious
                warehouses are strategically located in key transportation hubs,
                allowing for easy access to major roads, ports, and airports.
                This enables us to offer cost-effective and timely distribution
                services to our clients.
              </p>
            </div>
            <div class="secondPriContainerImage"></div>
            <div class="secondPriContainerDiv2">
              <p>DISCOVER</p>
              <div>
                <span class="material-symbols-sharp arrowEast">
                  north_east
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="subPriContainer">
        <div @click="toggleElement2" class="firstPriContainer">
          <div class="firstPriContainerDiv">
            <p>02</p>
            <p ref="moreTitle2">Transport and Logistics</p>
            <p>
              <span ref="moreArrow2" class="material-symbols-sharp">
                arrow_upward
              </span>
            </p>
          </div>
        </div>

        <div v-show="showElement2" class="secondPriContainer">
          <div class="secondPriContainerDiv">
            <div class="secondPriContainerPara">
              <p>
                We have various warehouses across countries facilitating the
                storage of our clients packages. we understand the critical role
                that warehousing plays in the logistics process. Our spacious
                warehouses are strategically located in key transportation hubs,
                allowing for easy access to major roads, ports, and airports.
                This enables us to offer cost-effective and timely distribution
                services to our clients.
              </p>
            </div>
            <div class="secondPriContainerImage secondPriContainerImage2"></div>
            <div class="secondPriContainerDiv2">
              <p>DISCOVER</p>
              <div>
                <span class="material-symbols-sharp arrowEast">
                  north_east
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="subPriContainer">
        <div @click="toggleElement3" class="firstPriContainer">
          <div class="firstPriContainerDiv">
            <p>03</p>
            <p ref="moreTitle3">Contract logistics</p>
            <p>
              <span ref="moreArrow3" class="material-symbols-sharp">
                arrow_upward
              </span>
            </p>
          </div>
        </div>

        <div v-show="showElement3" class="secondPriContainer">
          <div class="secondPriContainerDiv">
            <div class="secondPriContainerPara">
              <p>
                We have various warehouses across countries facilitating the
                storage of our clients packages. we understand the critical role
                that warehousing plays in the logistics process. Our spacious
                warehouses are strategically located in key transportation hubs,
                allowing for easy access to major roads, ports, and airports.
                This enables us to offer cost-effective and timely distribution
                services to our clients.
              </p>
            </div>
            <div class="secondPriContainerImage secondPriContainerImage3"></div>
            <div class="secondPriContainerDiv2">
              <p>DISCOVER</p>
              <div>
                <span class="material-symbols-sharp arrowEast">
                  north_east
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="preFooterDiv">
      <div class="firstPreFooterDiv">
        <p>Explore more</p>
        <p>logistics products</p>
      </div>
      <swiper-container
      class="sliderPreFooterDiv"
      :modules="modules"
        :slides-per-view="3"
        :pagination="{ clickable: true }"
        :scrollbar="{ draggable: true }"
        :breakpoints="{
          768: {
            slidesPerView: 2,
          },
        }"
      >
        <swiper-slide>Slide 1</swiper-slide>
        <swiper-slide>Slide 2</swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
      </swiper-container>
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import { ref } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination, Scrollbar, A11y } from "swiper";
import "swiper/css";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

const moreTitle = ref(null);
const moreTitle2 = ref(null);
const moreTitle3 = ref(null);
const moreArrow = ref(null);
const moreArrow2 = ref(null);
const moreArrow3 = ref(null);
const moreBody = ref(null);

export default {
  name: "HomePage",
  components: {
    Header,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      age: "",
      showElement: true,
      showElement2: false,
      showElement3: false,
    };
  },
  watch: {
    age() {
      console.log("Age:", this.age);
    },
  },

  methods: {
    toggleElement() {
      this.showElement = !this.showElement;
      if (this.showElement) {
        this.$refs.moreArrow.style.transition =
          "rotate .2s ease, color .5s ease-out";
        this.$refs.moreArrow.style.rotate = "180deg";
        this.$refs.moreArrow.style.color = "#ffcc00";
        this.$refs.moreTitle.style.transition = " color .5s ease-out";
        this.$refs.moreTitle.style.color = "#ffcc00";
        this.$refs.moreBody.style.transition =
          "visibility 5s ease, display 1s ease";
        // console.log(this.$refs.moreTitle.style);
      } else {
        this.$refs.moreArrow.style.rotate = "";
        this.$refs.moreTitle.style.color = "";
        this.$refs.moreArrow.style.color = "";
      }
      // myElement.value.style.color = myElement.value.style.color === 'white' ? 'red' : 'white';
      console.log(this.$refs.moreTitle.style);
    },

    toggleElement2() {
      this.showElement2 = !this.showElement2;
      if (this.showElement2) {
        this.$refs.moreArrow2.style.rotate = "180deg";
        this.$refs.moreArrow2.style.transition =
          "rotate .2s ease, color .5s ease-out";
        this.$refs.moreArrow2.style.color = "#ffcc00";
        this.$refs.moreTitle2.style.transition = " color .5s ease-out";
        this.$refs.moreTitle2.style.color = "#ffcc00";
      } else {
        this.$refs.moreArrow2.style.rotate = "";
        this.$refs.moreArrow2.style.color = "";
        this.$refs.moreTitle2.style.color = "";
      }
    },

    toggleElement3() {
      this.showElement3 = !this.showElement3;
      if (this.showElement3) {
        this.$refs.moreArrow3.style.transition =
          "rotate .2s ease, color .5s ease-out";
        this.$refs.moreArrow3.style.rotate = "180deg";
        this.$refs.moreArrow3.style.color = "#ffcc00";
        this.$refs.moreTitle3.style.transition = "color .5s ease-out";
        this.$refs.moreTitle3.style.color = "#ffcc00";
      } else {
        this.$refs.moreArrow3.style.rotate = "";
        this.$refs.moreArrow3.style.color = "";
        this.$refs.moreTitle3.style.color = "";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/global.scss";
@import "@/styles/header.scss";
@import "@/styles/homepage.scss";
</style>
