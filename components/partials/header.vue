<template>
  <clean-card>
    <v-container>
      <v-card-actions class="pa-0">
        <v-btn class="text--lighten-2" text @click="routing('/')">Главная</v-btn>
        <v-btn class="text--lighten-2" text @click="routing('/catalog/')">Каталог</v-btn>
        <v-spacer/>

        <v-text-field style="max-width: 250px"
                      append-icon="mdi-magnify"
                      dense outlined hide-details/>

        <v-btn class="text--lighten-2" text>
          <v-icon>mdi-heart-outline</v-icon>
        </v-btn>

        <v-btn class="text--lighten-2" text>
          <v-icon>mdi-chart-box-outline</v-icon>
        </v-btn>

        <v-btn class="text--lighten-2" text>
          <v-icon>mdi-account-outline</v-icon>
        </v-btn>

        <v-btn class="text--lighten-2" text
               style="text-transform: none">
          <v-icon>mdi-cart-outline</v-icon>
          <div style="margin-left: 10px; font-size: 12px; color: #85e783">
            <span>15 000</span>
            <v-icon style="font-size: 12px !important;">mdi-currency-rub</v-icon>
          </div>
        </v-btn>
      </v-card-actions>
    </v-container>
  </clean-card>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Header extends Vue {
  routing (link: string) {
    this.$router.push (link)
  }
}
</script>
