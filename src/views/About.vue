<template>
  <div class="about">
    <br>

    <h1 class="title1">{{ $t("companyProfile") }}</h1>
    <br>

    <div class="subTitle1">
      {{$t("subtitleAboutUs")}}
    </div>
    <br>
    <div class="subTitle1">
      {{$t("subtitleAboutUs1")}}
    </div>
    <br>
    <br>
    <h1 class="title1">{{ $t("vision") }}</h1>
    <span class="subTitle1" style="font-size: 25px;font-weight: bold;text-transform: uppercase">
      {{$t("vision1")}}
    </span>
    <br>
    <br>

    <h1 class="title1">{{ $t("mission") }}</h1>
    <v-row>
      <v-col cols="12" md="2" sm="2"></v-col>
      <v-col cols="12" md="10" sm="10">
        <div class="title2" style="text-align: left">
          {{$t("mission0")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("mission1")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("mission2")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("mission3")}}
        </div>

      </v-col>
    </v-row>
    <br>
    <h1 class="title1">{{ $t("coreValue") }}</h1>

    <v-row>
      <v-col cols="12" md="2" sm="2"></v-col>
      <v-col cols="12" md="10" sm="10">
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("coreValue1")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("coreValue2")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("coreValue3")}}
        </div>
        <div class="subTitle2">
          <v-icon class="iconColor">mdi-star-four-points</v-icon> {{$t("coreValue4")}}
        </div>
      </v-col>
    </v-row>

  </div>
</template>
