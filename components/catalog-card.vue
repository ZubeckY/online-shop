<template>
  <v-hover v-slot="{ hover }">
    <v-card :elevation="hover ? 12 : 0"
            rounded="0"
            width="100%"
            max-width="250px"
            @click="routing(`/catalog/prop`)"
            style="margin: 0 15px 20px">

      <v-card-actions style="min-height: 48px">
        <v-spacer/>
        <v-chip v-if="isHit">Хит</v-chip>
        <v-chip v-if="isDiscount">Скидка</v-chip>
      </v-card-actions>

      <div>
        <v-img max-height="150"
               max-width="250"
               src="data:image/jpeg;base64,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">
        </v-img>
      </div>

      <v-card-text class="pa-2 pb-0 ma-0">Название куска мыла</v-card-text>

      <v-card-actions>
        <v-rating value="4.5" readonly half-increments small></v-rating>
        <v-spacer></v-spacer>
        <v-btn icon x-small @click.stop>
          <v-icon>mdi-scale-unbalanced</v-icon>
        </v-btn>

        <v-btn icon x-small @click.stop>
          <v-icon>mdi-heart-outline</v-icon>
        </v-btn>
      </v-card-actions>

      <v-card-actions class="ma-0 px-0 pb-1">
        <v-card-title class="justify-center pa-0 pl-2">
          <span :class="isDiscount ? 'text-decoration-line-through error--text pr-3' : ''">1 000</span>
          <span v-if="isDiscount">990</span>
          <v-icon small>mdi-currency-rub</v-icon>
        </v-card-title>
        <v-spacer/>
        <v-btn @click.stop text
               color="success"
               class="text--lighten-2"
               style="text-transform: none">
          В корзину
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-hover>
</template>
<script lang="ts">
import {Component, Prop, Vue} from "vue-property-decorator"
@Component
export default class CustomCard extends Vue {
  isHit:boolean = true
  isDiscount:boolean = true

  routing (link:string) {
    this.$router.push(link)
  }
}
</script>
<style scoped>
.v-card {
  transition: box-shadow .3s ease-in-out;
}
</style>
