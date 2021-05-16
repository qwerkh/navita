<template>
  <div class="home">
    <h1 class="title1">{{ $t('welcome') }}</h1>
    <h3>{{ $t('slogan') }}</h3>
    <br>
    <hr style="color: green; height: 3px !important;">
    <br>
    <br>
    <h2 class="title1">{{ $t("navitaExistingProduct") }}</h2>
    <br>
    <v-row>
      <v-col sm="6" md="6" cols="12" v-if="$vuetify.breakpoint.mobile">
        <br><br><br><br>
        <h2 class="title1">{{ $t("dragonFruit") }}</h2>
        <div class="subTitle1">{{ $t('subtitleDragonFruit') }}</div>
        <v-row>
          <v-col sm="5" cols="5" md="5">
            <v-list>
              <v-list-item v-for="(d ,i) in dragonFruitList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: green">mdi-checkbox-marked-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col sm="7" cols="7" md="7">
            <v-list>
              <v-list-item v-for="(d ,i) in dragonFruitDistList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: red">mdi-close-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>

        </v-row>
      </v-col>
      <v-col sm="6" md="6" cols="12">
        <v-img src="../assets/i_dragron_fruit.jpg"></v-img>
      </v-col>

      <v-col sm="6" md="6" cols="12" v-if="!$vuetify.breakpoint.mobile">
        <h2 class="title1">{{ $t("dragonFruit") }}</h2>
        <div class="subTitle1">{{ $t('subtitleDragonFruit') }}</div>
        <v-row>
          <v-col sm="5" cols="5" md="5">

            <v-list>
              <v-list-item v-for="(d ,i) in dragonFruitList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: green">mdi-checkbox-marked-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col sm="7" cols="7" md="7">

            <v-list>
              <v-list-item v-for="(d ,i) in dragonFruitDistList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: red">mdi-close-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>

        </v-row>
      </v-col>
      <br>
      <br>
      <br>
      <br>
      <v-col sm="6" md="6" cols="12" v-if="!$vuetify.breakpoint.mobile">
        <h2 class="title1">{{ $t("pineapple") }}</h2>
        <div class="subTitle1">{{ $t('subtitlePineapple') }}</div>

        <v-row>
          <v-col sm="5" cols="5" md="5">
            <v-list>
              <v-list-item v-for="(d ,i) in pineappleList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: green">mdi-checkbox-marked-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col sm="7" cols="7" md="7">
            <v-list>
              <v-list-item v-for="(d ,i) in pineappleDistList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: red">mdi-close-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>

        </v-row>
      </v-col>
      <v-col sm="6" md="6" cols="12" v-if="!$vuetify.breakpoint.mobile">
        <v-img src="../assets/i_pineapple.jpg"></v-img>
      </v-col>

      <v-col sm="6" md="6" cols="12" v-if="$vuetify.breakpoint.mobile">

        <h2 class="title1">{{ $t("pineapple") }}</h2>
        <div class="subTitle1">{{ $t('subtitlePineapple') }}</div>
        <v-row>
          <v-col sm="5" cols="5" md="5">
            <v-list>
              <v-list-item v-for="(d ,i) in pineappleList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: green">mdi-checkbox-marked-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col sm="7" cols="7" md="7">
            <v-list>
              <v-list-item v-for="(d ,i) in pineappleDistList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: red">mdi-close-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>

        </v-row>
      </v-col>

      <v-col sm="6" md="6" cols="12" v-if="$vuetify.breakpoint.mobile">
        <v-img src="../assets/i_pineapple.jpg"></v-img>
      </v-col>
      <br>
      <br>
      <br>
      <v-col sm="6" md="6" cols="12" v-if="!$vuetify.breakpoint.mobile">
        <v-img src="../assets/i_mango.jpg"></v-img>
      </v-col>
      <v-col sm="6" md="6" cols="12">
        <h2 class="title1">{{ $t("mango") }}</h2>
        <div class="subTitle1">{{ $t('subtitleMango') }}</div>
        <v-row>
          <v-col sm="5" cols="5" md="5">
            <v-list>
              <v-list-item v-for="(d ,i) in mangoList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: green">mdi-checkbox-marked-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col sm="7" cols="7" md="7">
            <v-list>
              <v-list-item v-for="(d ,i) in mangoDistList" :key="i">
                <v-list-item-content style="text-align: left;height: 48px !important;">
                  <v-list-item-title>
                    <v-icon style="color: red">mdi-close-circle</v-icon>
                    {{ $t(d) }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>

        </v-row>
      </v-col>
      <v-col sm="6" md="6" cols="12" v-if="$vuetify.breakpoint.mobile">
        <v-img src="../assets/i_mango.jpg"></v-img>
      </v-col>
    </v-row>

    <br>
    <br>
    <hr style="color: green; height: 3px !important;">
    <br>

    <h2 class="title1">{{ $t("whyNavita") }}</h2>
    <br>
    <br>
    <div v-if="language=='en'">
      <img src="../assets/Compare pineapple_English.jpg"/>
      <br>
      <br>
      <img src="../assets/compare Mango_English.jpg"/>
    </div>

    <div v-if="language=='km'">

      <img src="../assets/Compare pineapple_khmer.jpg"/>
      <br>
      <br>
      <img src="../assets/compare Mango_khmer.jpg"/>
    </div>
    <br>
    <br>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data() {
    return {
      language: "",
      dragonFruitList: [
        "calcium",
        "vitaminB1",
        "vitaminB2",
        "vitaminB3",
        "vitaminC",
        "vitaminE"
      ],
      dragonFruitDistList: [
        "sugarsAdded",
        "colorAdded",
        "preservatives"
      ],
      pineappleList:[
        "calcium",
        "vitaminA",
        "vitaminB",
        "vitaminC",
        "vitaminE"
      ],
      pineappleDistList:[
        "sugarsAdded",
        "colorAdded",
        "preservatives"
      ],
      mangoList:[
        "calcium",
        "vitaminB1",
        "vitaminB2",
        "vitaminB3",
        "vitaminC",
        "vitaminE"
      ],
      mangoDistList:[
        "sugarsAdded",
        "colorAdded",
        "preservatives"
      ]
    }
  },
  watch: {
    "$i18n.locale"(val) {
      this.language = val;
    }
  },
  created() {
    this.language = this.$i18n.locale;
  }
}
</script>
