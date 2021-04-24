<template>
  <div class="home">
    <h1 class="title1">{{ $t('welcome') }}</h1>
    <h3>{{ $t('slogan') }}</h3>
    <br>
    <hr style="color: green; height: 3px !important;">
    <br>
    <br>
    <h2 class="title1">{{$t("navitaExistingProduct")}}</h2>
    <v-row>
      <v-col sm="6" md="6" cols="12">
        <v-img src="../assets/i_dragron_fruit.jpg"></v-img>
      </v-col>
      <v-col sm="6" md="6" cols="12">
        <br><br><br><br>
        <h2 class="title1">{{$t("dragonFruit")}}</h2>
        {{$t('subtitleDragonFruit')}}
      </v-col>
      <br>
      <br>
      <v-col sm="6" md="6" cols="12"  v-if="!$vuetify.breakpoint.mobile">
        <br><br><br><br>

        <h2 class="title1">{{$t("pineapple")}}</h2>
        <span class="subTitle1">{{$t('subtitlePineapple')}}</span>
      </v-col>
      <v-col sm="6" md="6" cols="12">
        <v-img src="../assets/i_pineapple.jpg"></v-img>
      </v-col>

      <v-col sm="6" md="6" cols="12" v-if="$vuetify.breakpoint.mobile">
        <br><br><br><br>

        <h2 class="title1">{{$t("pineapple")}}</h2>
        <span class="subTitle1">{{$t('subtitlePineapple')}}</span>
      </v-col>
      <br>
      <br>
      <v-col sm="6" md="6" cols="12">
        <v-img src="../assets/i_mango.jpg"></v-img>
      </v-col>
      <v-col sm="6" md="6" cols="12">
        <br><br><br><br>
        <h2 class="title1">{{$t("mango")}}</h2>
        <span class="subTitle1">{{$t('subtitleMango')}}</span>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
}
</script>
