<template>
  <div id="app" class="overflow-hidden" data-app style="font-family: 'Khmer OS Battambang'">
    <v-app-bar
        fixed
        dark
        :style="$vuetify.breakpoint.mobile ? 'height: 40px !important;background: darkcyan;padding-left: 0px !important;padding-right: 0px !important;margin:0px !important' : 'height: 40px !important;background: darkcyan;padding-left: 40px !important;padding-right: 40px !important;'"
        class="fixTitle"
    >
      <h5>
        <v-icon style="font-size: 15px">mdi-phone</v-icon>
        (855) 96 47 77 456
        <v-icon style="font-size: 15px;padding-left: 50px">mdi-email</v-icon>info@navitafood.com
      </h5>
      <v-spacer/>
      <v-btn icon @click="changeLanguage()" v-if="!$vuetify.breakpoint.mobile">
        <v-img v-if="language==='en'" style="height: 20px !important;width: 20px !important;"
               src="https://upload.wikimedia.org/wikipedia/en/a/a4/Flag_of_the_United_States.svg"></v-img>
        <v-img v-if="language==='km'" style="height: 20px !important;width: 20px !important;"
               src="https://upload.wikimedia.org/wikipedia/commons/8/83/Flag_of_Cambodia.svg"></v-img>
      </v-btn>
      <v-btn icon class="mx-4 white--text"  v-if="!$vuetify.breakpoint.mobile"
             href="https://www.facebook.com/Navita-Food-Production-100351005124515/" target="_blank">
        <v-icon size="24px">mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon class="mx-4 white--text"  v-if="!$vuetify.breakpoint.mobile"
             href="https://t.me/joinchat/1Gv8yCmnGwVjZGQ1" target="_blank">
        <v-icon size="24px">mdi-telegram</v-icon>
      </v-btn>

    </v-app-bar>
    <v-app-bar
        fixed
        dark
        class="appBar"
        style="opacity: 0.4;margin-top: 40px; !important;"

    >
    </v-app-bar>
    <v-app-bar
        fixed
        dark
        style="background: transparent;margin-top: 40px !important;"
    >
      <template v-slot:img="{ props }">
        <v-img
            style="height: 100%;"
            v-bind="props"
            gradient="to top right, rgba(0,0,0,.0), rgba(0,0,0,.0)"
        >
        </v-img>
      </template>
      <h3>Navita</h3>
      <v-spacer></v-spacer>

      <v-btn icon @click="changeLanguage()" v-if="$vuetify.breakpoint.mobile">
        <v-img v-if="language==='en'" style="height: 20px !important;width: 20px !important;"
               src="https://upload.wikimedia.org/wikipedia/en/a/a4/Flag_of_the_United_States.svg"></v-img>
        <v-img v-if="language==='km'" style="height: 20px !important;width: 20px !important;"
               src="https://upload.wikimedia.org/wikipedia/commons/8/83/Flag_of_Cambodia.svg"></v-img>
      </v-btn>
      <v-btn icon class="mx-4 white--text" href="https://www.facebook.com/Navita-Food-Production-100351005124515/"
             target="_blank">
        <v-icon size="24px" v-if="$vuetify.breakpoint.mobile">mdi-facebook</v-icon>
      </v-btn>

      <v-btn icon class="mx-4 white--text" href="https://t.me/joinchat/1Gv8yCmnGwVjZGQ1"
             target="_blank">
        <v-icon size="24px" v-if="$vuetify.breakpoint.mobile">mdi-telegram</v-icon>
      </v-btn>


      <v-menu offset-y v-if="$vuetify.breakpoint.mobile">
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs"
                 v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item to="/">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>&nbsp;&nbsp; {{ $t('home') }}</v-list-item-title>
          </v-list-item>
          <v-list-item to="/about">
            <v-list-item-icon>
              <v-icon>mdi-information-variant</v-icon>
            </v-list-item-icon>
            <v-list-item-title>&nbsp;&nbsp; {{ $t('about') }}</v-list-item-title>
          </v-list-item>
          <v-list-item to="/contact">
            <v-list-item-icon>
              <v-icon>mdi-message</v-icon>
            </v-list-item-icon>
            <v-list-item-title>&nbsp;&nbsp; {{ $t('contactUs') }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-tabs
          v-if="!$vuetify.breakpoint.mobile"
          align-with-title
          centered
          style="margin-left: 30%"
      >
        <v-tabs-slider color="yellow"></v-tabs-slider>
        <v-tab to="/"
        >
          <v-icon>mdi-home</v-icon>
          {{ $t('home') }}
        </v-tab>
        <v-tab to="/about"
        >
          <v-icon>mdi-information-variant</v-icon>
          {{ $t('about') }}
        </v-tab>
        <v-tab to="/contact"
        >
          <v-icon>mdi-message</v-icon>
          {{ $t('contactUs') }}
        </v-tab>

      </v-tabs>


      <!--            <v-btn class="toolbarTitle">
                      <v-icon>mdi-home</v-icon>
                      {{$t('home')}}
                  </v-btn>

                  <v-btn class="toolbarTitle">
                      <v-icon>mdi-heart</v-icon>
                      {{$t('about')}}

                  </v-btn>

                  <v-btn class="toolbarTitle">
                      <v-icon>mdi-dots-vertical</v-icon>
                      {{$t('contactUs')}}

                  </v-btn>-->
    </v-app-bar>

    <v-carousel
        :cycle="cycle"
        :show-arrows="false"
        hide-delimiter-background
    >
      <v-carousel-item
          v-if="!$vuetify.breakpoint.mobile"
          key="121"
          reverse-transition="fade-transition"
          background-size="contain"
          transition="slide-x-transition"
          src="./assets/slider0.jpg"
      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          v-if="$vuetify.breakpoint.mobile"
          key="121"
          reverse-transition="fade-transition"
          background-size="contain"
          transition="slide-x-transition"
          src="./assets/slider0m.jpg"
      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          v-if="$vuetify.breakpoint.mobile"
          key="1"
          reverse-transition="fade-transition"
          background-size="contain"
          transition="slide-x-transition"
          src="./assets/slider1m.jpg"
      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          v-if="!$vuetify.breakpoint.mobile"

          key="1"
          reverse-transition="fade-transition"
          background-size="contain"
          transition="slide-x-transition"
          src="./assets/slider1.jpg"
      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          v-if="!$vuetify.breakpoint.mobile"

          key="2"
          background-size="contain"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
          src="./assets/slider2.jpg"

      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="2"
          v-if="$vuetify.breakpoint.mobile"
          background-size="contain"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
          src="./assets/slider2m.jpg"

      >
        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="3"
          v-if="!$vuetify.breakpoint.mobile"

          background-size="contain"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
          src="./assets/slider3.jpg"


      >
        <!--        <v-img src="./assets/slider3.jpg" contain width="100%"></v-img>-->

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="3"
          v-if="$vuetify.breakpoint.mobile"

          background-size="contain"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
          src="./assets/slider3m.jpg"


      >
        <!--        <v-img src="./assets/slider3.jpg" contain width="100%"></v-img>-->

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="4"
          v-if="!$vuetify.breakpoint.mobile"

          background-size="contain"
          src="./assets/slider4.jpg"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
      >

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="4"
          v-if="$vuetify.breakpoint.mobile"

          background-size="contain"
          src="./assets/slider4m.jpg"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
      >

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="5"
          v-if="!$vuetify.breakpoint.mobile"

          src="./assets/slider5.jpg"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
      >

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
      <v-carousel-item
          key="5"
          v-if="$vuetify.breakpoint.mobile"
          src="./assets/slider5m.jpg"
          reverse-transition="fade-transition"
          transition="slide-x-transition"
      >

        <div class="absolute-div">
          <div class="carousel-caption">
            <!--                        <h1>Slide {{1 }} </h1>-->
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>

    <v-sheet
        id="scrolling-techniques-3"
        class="overflow-y-auto"
        max-height="600"
    >
      <v-container style="min-height: 1000px;">
        <router-view></router-view>

      </v-container>
      <v-footer
          dark
          padless
      >
        <v-card
            flat
            tile
            class="text-center"
            style="background-color: teal;border-color: teal"
        >
          <v-card-text>
            <v-btn
                v-for="d in icons"
                :key="d.icon"
                class="mx-4 white--text"
                :href="d.url"
                icon
                target="_blank"
            >
              <v-icon size="24px">
                {{ d.icon }}
              </v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="white--text pt-0" v-if="$vuetify.breakpoint.mobile">
            {{$t('footer')}}
          </v-card-text>
          <v-card-text class="white--text pt-0" v-if="!$vuetify.breakpoint.mobile" style="padding-left: 15%;padding-right: 15%">
            {{$t('footer')}}
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            @copyright 2021 — <strong>Navita</strong>
          </v-card-text>
        </v-card>
      </v-footer>

    </v-sheet>


  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      items: [
        {
          src: './assets/slider1.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
      cycle: true,
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
      language: "en",
      icons: [
        {
          icon: 'mdi-facebook',
          url: "https://www.facebook.com/Navita-Food-Production-100351005124515/"
        },
        {
          icon: 'mdi-telegram',
          url: "https://t.me/joinchat/1Gv8yCmnGwVjZGQ1"
        }
      ],
    }
  },
  methods: {
    changeLanguage() {
      let vm = this;
      vm.language = vm.language === "en" ? "km" : "en";
      this.$i18n.locale = vm.language;
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.appBar {
  margin-top: 40px !important;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.carousel-caption {
  position: absolute;
  z-index: 1;
  display: table;
  width: 100%;
  height: 100%;
}

.absolute-div {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.carousel-caption h1 {
  font-size: 60px !important;
  display: table-cell;
  vertical-align: middle;
  text-align: center;
}

.fixTitle .v-toolbar__content {
  height: 40px !important;
}

.iconTitle {
  font-size: 20px !important;
  padding-left: 20px;
  cursor: pointer;
}

.toolbarTitle {
  padding-right: 40px !important;
  background: transparent;
  color: transparent;
}

.title1 {
  color: teal;
}

.title2 {
  color: teal;
}

.subTitle1 {
  size: 12px;
}

.subTitle2 {
  size: 12px;
  text-align: left !important;
}

.iconColor {
  color: green !important;
}

.v-list-item .v-list-item__title, .v-list-item .v-list-item__subtitle {
  line-height: 2.2 !important;
}

</style>
