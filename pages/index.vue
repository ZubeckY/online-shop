<template>
  <div>
    <slider/>

    <clean-card>
      <v-container>
        <v-card-title>У нас покупают</v-card-title>
        <div class="d-flex flex-row flex-wrap">
          <catalog-card v-for="i in 8" :key="i"></catalog-card>
        </div>
      </v-container>
    </clean-card>

    <div>
      <v-container>
        <v-card-title>Скидки</v-card-title>
        <div class="d-flex flex-row flex-wrap">
          <catalog-card v-for="i in 4" :key="i"></catalog-card>
        </div>
      </v-container>
    </div>

    <warranty-list/>

    <div>
      <v-container>
        <v-card-title>Выгодные предложения</v-card-title>
        <div class="d-flex flex-row flex-wrap">
          <catalog-card v-for="i in 4" :key="i"></catalog-card>
        </div>
      </v-container>
    </div>

    <partials-footer-mailing-form/>

  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Pages extends Vue {
}
</script>
