<template>
    <div id="app" class="overflow-hidden">

        <v-app-bar
                fixed
                dark
                style="height: 40px !important;background: darkcyan;padding-left: 40px !important;padding-right: 40px !important;"
                class="fixTitle"
        >
            <h5>
                <v-icon style="font-size: 15px">mdi-phone</v-icon>
                (855) 96 47 77 456
                <v-icon style="font-size: 15px;padding-left: 50px">mdi-email</v-icon>
                info@navitafood.com
            </h5>
            <v-spacer/>
                <v-icon class="iconTitle">mdi-facebook</v-icon>

                <v-icon  class="iconTitle">mdi-twitter</v-icon>
                <v-icon class="iconTitle">mdi-telegram</v-icon>

        </v-app-bar>
        <v-app-bar
                fixed
                dark
                style="opacity: 0.4;margin-top: 40px;"

        >
        </v-app-bar>

        <v-app-bar
                fixed
                dark
                style="background: transparent;margin-top: 40px"
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

            <v-tabs
                    align-with-title
            >
                <v-tabs-slider color="yellow"></v-tabs-slider>
                <v-tab
                >
                    <v-icon>mdi-home</v-icon>
                    {{$t('home')}}
                </v-tab>
            </v-tabs>
            <v-btn class="toolbarTitle">
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

            </v-btn>
        </v-app-bar>

        <v-carousel
                :cycle="cycle"
                :show-arrows="false"
                hide-delimiter-background
        >
            <v-carousel-item
                    v-for="(item, i) in items"
                    :key="i"
                    :src="item.src"
                    reverse-transition="fade-transition"
                    transition="slide-x-transition"
            >

                <div class="absolute-div">
                    <div class="carousel-caption">
                        <h1>Slide {{ i + 1 }} </h1>
                    </div>
                </div>
            </v-carousel-item>
        </v-carousel>

        <v-sheet
                id="scrolling-techniques-3"
                class="overflow-y-auto"
                max-height="600"
        >
            <v-container style="height: 1000px;">
                <router-view></router-view>
            </v-container>
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
                        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
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

    .iconTitle{
      font-size: 20px !important;
      padding-left: 20px;
      cursor: pointer;
    }

    .toolbarTitle{
        padding-right: 40px !important;
        background: transparent;
        color: transparent;
    }

</style>
