<template>
  <div class="messages">

    <!-- Header -->
    <el-row>
      <el-col :xs="2" :sm="2" :md="2" :lg="2" :xl="2">
        <el-button @click="goBack()" class="back_button" type="danger" circle
                   icon="el-icon-d-arrow-left"></el-button>
      </el-col>
      <el-col :xs="24" :sm="24" :md="24" :lg="24" :xl="24">
        <h1 style="margin-left: 50px">Our Stories With You </h1>
      </el-col>
    </el-row>

    <!-- Content -->
    <el-row type="flex" justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <div class="block" style="overflow:auto; min-height: 70vh">

          <loading :active="loaderLoading"
                   :is-full-page="loaderFullPage"
                   :color="loaderColor"
                   :opacity="loaderOpacity"
                   :height="loaderHeight"
                   :width="loaderWidth"
                   :loader="loaderStyle"></loading>

          <transition name="el-zoom-in-bottom">
            <el-timeline class="messages_timeline"
                         v-show="showTimeline">

              <el-timeline-item timestamp="20230520" placement="top">
                <el-card>
                  <el-image :src="img25" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3> Our first ever meet up. Dito talaga nag simula ang lahat 🤣</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="Skating Era !!" placement="top">
                <el-card>
                  <el-image :src="img2" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="Si Kuya na game na game na kuhanan tayo ng pics" placement="top">
                <el-card>
                  <el-image :src="img26" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img36" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img37" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img35" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <el-image :src="img1" @load="onImgLoad"></el-image>
                  <h3>Our last stop for that day is in arcade. <br>
                    Ang aming singerist Kkyu 🎶!!</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img34" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img33" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>❤️ ❤️ ❤️</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="20230527" placement="top">
                <el-card>
                  <el-image :src="img14" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>Nainggit yung iba kaya nag karoon nito  🤣</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="20230527" placement="top">
                <el-card>
                  <el-image :src="img5" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img6" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img7" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img8" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img9" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img10" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img11" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img13" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img27" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img28" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img31" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>


              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img15" @load="onImgLoad"></el-image>
                  <h3>This day might be a bit short. <br>
                    But all had fun 😎</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img12" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>❤️ ❤️ ❤️</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="20230828" placement="top">
                <el-card>
                  <el-image :src="img16" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>Get together na may konting surprise 😉</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img24" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img17" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img22" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
              <el-card>
                <el-image :src="img23" @load="onImgLoad"></el-image>
              </el-card>
            </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img18" @load="onImgLoad"></el-image>
                  <h3>Mga ayaw pang umuwi... Pero masakit na paa natin nito 😂</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>❤️ ❤️ ❤️</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="20231015" placement="top">
                <el-card>
                  <el-image :src="img21" @load="onImgLoad"></el-image>
                  <h3>CSE</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img19" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img20" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img38" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img39" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img40" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img41" @load="onImgLoad"></el-image>
                  <h3>To more CSE... <br> Specially yung kay Jungwon 😂</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>❤️ ❤️ ❤️</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="20231015" placement="top">
                <el-card>
                  <el-image :src="img32" @load="onImgLoad"></el-image>
                  <h3>We always wanna see you all smiles and happy 😁</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img29" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img45" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img44" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img43" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item placement="top">
                <el-card>
                  <el-image :src="img42" @load="onImgLoad"></el-image>
                </el-card>
              </el-timeline-item>

              <el-timeline-item>
                <el-card>
                  <h3>❤️ ❤️ ❤️</h3>
                </el-card>
              </el-timeline-item>

              <el-timeline-item timestamp="Cause there will be a lot more memories to come. 😏" placement="bottom">
                <el-card>
                  <h3>To be continued...</h3>
                </el-card>
              </el-timeline-item>

            </el-timeline>
          </transition>
        </div>
      </el-col>
    </el-row>

  </div>
</template>

<script>
// Loading effect component
import Loading from 'vue-loading-overlay';
import 'vue-loading-overlay/dist/vue-loading.css';
// Images
// TODO : Put your images in /src/assets, and import them accordingly.
import img1 from '../assets/images/img-1.jpg'
import img2 from '../assets/images/img-2.jpg'
import img3 from '../assets/images/img-3.jpg'
import img4 from '../assets/images/img-4.jpg'
import img5 from '../assets/images/img-5.jpg'
import img6 from '../assets/images/img-6.jpg'
import img7 from '../assets/images/img-7.jpg'
import img8 from '../assets/images/img-8.jpg'
import img9 from '../assets/images/img-9.jpg'
import img10 from '../assets/images/img-10.jpg'
import img11 from '../assets/images/img-11.jpg'
import img12 from '../assets/images/img-12.jpg'
import img13 from '../assets/images/img-13.jpg'
import img14 from '../assets/images/img-14.jpg'
import img15 from '../assets/images/img-15.jpg'
import img16 from '../assets/images/img-16.jpg'
import img17 from '../assets/images/img-17.jpg'
import img18 from '../assets/images/img-18.jpg'
import img19 from '../assets/images/img-19.jpg'
import img20 from '../assets/images/img-20.jpg'
import img21 from '../assets/images/img-21.jpg'
import img22 from '../assets/images/img-22.jpg'
import img23 from '../assets/images/img-23.jpg'
import img24 from '../assets/images/img-24.jpg'
import img25 from '../assets/images/img-25.jpg'
import img26 from '../assets/images/img-26.jpg'
import img27 from '../assets/images/img-27.jpg'
import img28 from '../assets/images/img-28.jpg'
import img29 from '../assets/images/img-29.jpg'
import img30 from '../assets/images/img-30.jpg'
import img31 from '../assets/images/img-31.jpg'
import img32 from '../assets/images/img-32.jpg'
import img33 from '../assets/images/img-33.jpg'
import img34 from '../assets/images/img-34.jpg'
import img35 from '../assets/images/img-35.jpg'
import img36 from '../assets/images/img-36.jpg'
import img37 from '../assets/images/img-37.jpg'
import img38 from '../assets/images/img-38.jpg'
import img39 from '../assets/images/img-39.jpg'
import img40 from '../assets/images/img-40.jpg'
import img41 from '../assets/images/img-41.jpg'
import img42 from '../assets/images/img-42.jpg'
import img43 from '../assets/images/img-43.jpg'
import img44 from '../assets/images/img-44.jpg'
import img45 from '../assets/images/img-45.jpg'

export default {
  name: "Messages",
  data() {
    return {
      // Display Timeline
      showTimeline: false,
      // Images
      // TODO : Modify the variables to cooperate with your images
      img1: img1,
      img2: img2,
      img3: img3,
      img4: img4,
      img5: img5,
      img6: img6,
      img7: img7,
      img8: img8,
      img9: img9,
      img10: img10,
      img11: img11,
      img12: img12,
      img13: img13,
      img14: img14,
      img15: img15,
      img16: img16,
      img17: img17,
      img18: img18,
      img19: img19,
      img20: img20,
      img21: img21,
      img22: img22,
      img23: img23,
      img24: img24,
      img25: img25,
      img26: img26,
      img27: img27,
      img28: img28,
      img29: img29,
      img30: img30,
      img31: img31,
      img32: img32,
      img33: img33,
      img34: img34,
      img35: img35,
      img36: img36,
      img37: img37,
      img38: img38,
      img39: img39,
      img40: img40,
      img41: img41,
      img42: img42,
      img43: img43,
      img44: img44,
      img45: img45,
      imagesLoaded: 0,
      // TODO : Modify this number (totalImages) to the images you use in the content
      totalImages : 6,
      // Loader
      loaderLoading: true,
      loaderColor: "#dd6161",
      loaderOpacity: 1,
      loaderStyle: "dots",
      loaderHeight: 60,
      loaderWidth: 60,
      loaderFullPage: false
    }
  },
  components: {
    Loading
  },
  methods: {
    goBack() {
      this.$router.go(-1);
    },
    // This is a dump version of loading function,
    // feel free to change it to a more elegant implementation.
    onImgLoad() {
      this.imagesLoaded += 1;
      if (this.imagesLoaded === this.totalImages) {
        console.log("Images Loaded");
        setTimeout(() => this.loaderLoading = false, 500);
        setTimeout(() => this.showTimeline = true, 800);
      }
    }
  }
}
</script>

<style scoped>
.messages_timeline {
  width: 80%;
  height: 83vh;
  margin-left: auto;
  margin-right: auto;
}

.back_button {
  margin-top: 15px;
  position: absolute;
}
</style>
