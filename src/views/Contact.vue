<template>
  <div class="about">
    <h1 class="title1" style="text-align: left;color: #F69946;">{{ $t("contactUs") }}</h1>
    <h2 class="title1" style="text-align: left">
      {{ $t("getInTouch") }}
    </h2>
    <v-row>
      <v-col cols="12" md="6" sm="6">
        <div class="subTitle1" style="text-align: left">
          {{ $t("getInTouchDetail") }}
        </div>

        <v-list two-line>
          <template>
            <v-list-item>
              <v-list-item-action>
                <v-btn fab style="color: green">
                  <v-icon>mdi-map-marker-radius</v-icon>
                </v-btn>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>{{ $t("visitUs") }}</v-list-item-title>
                <v-list-item-subtitle>{{ $t("addressInfo") }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </template>
        </v-list>
        <v-list two-line>
          <template>
            <v-list-item>
              <v-list-item-action>
                <v-btn fab style="color: green">
                  <v-icon>mdi-email</v-icon>
                </v-btn>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>{{ $t("mailUs") }}</v-list-item-title>
                <v-list-item-subtitle>info@navitafood.com</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </template>
        </v-list>
        <v-list two-line>
          <template>
            <v-list-item>
              <v-list-item-action>
                <v-btn fab style="color: green">
                  <v-icon>mdi-phone</v-icon>
                </v-btn>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>{{ $t("callUs") }}</v-list-item-title>
                <v-list-item-subtitle>(855) 96 47 77 456</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </template>
        </v-list>
      </v-col>

      <v-col cols="12" md="6" sm="6">
          <v-img src="../assets/dFruit.gif"></v-img>
      </v-col>
    </v-row>
  </div>
</template>
