<template>
  <v-container>
    <v-breadcrumbs :items="items" divider="-"></v-breadcrumbs>

    <clean-card v-if="cart.length">

    </clean-card>

    <clean-card v-else class="text-center pa-16">
      <div>
        <v-icon style="font-size: 80px">mdi-cart-outline</v-icon>
      </div>
      <v-card-text>
        В вашей корзине пока пусто
      </v-card-text>

      <v-btn color="success" class="text--lighten-2"
             style="text-transform: none"
             @click="routing('/catalog')">
        Перейти к покупкам
      </v-btn>
    </clean-card>


  </v-container>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Cart extends Vue {
  cart = []

  items = [
    {
      text: 'Главная',
      disabled: false,
      href: '/',
    },
    {
      text: 'Корзина',
      disabled: false,
      href: '/cart',
    },
  ]

  routing (link:string) {
    this.$router.push(link)
  }
}
</script>
