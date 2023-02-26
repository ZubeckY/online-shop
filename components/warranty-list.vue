<template>
  <clean-card>
    <v-container>
      <v-row class="pt-3">

        <v-col class="text-center" v-for="(item, i) in list" :key="i">
          <v-icon color="success" class="text--lighten-2" style="font-size: 45px">{{ item.icon }}</v-icon>
          <v-card-title class="justify-center pb-0" style="font-size: 16px">{{ item.title }}</v-card-title>
          <v-card-text style="font-size: 12px">{{ item.text }}</v-card-text>
        </v-col>

      </v-row>
    </v-container>
  </clean-card>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"

@Component
export default class WarrantyList extends Vue {

  list = [
    {
      icon: 'mdi-truck-fast-outline',
      title: 'Бесплатная доставка',
      text: 'Бесплатная доставка по России при сумме заказа от 3000 руб.',
    },
    {
      icon: 'mdi-clock-fast',
      title: 'Поддержка 24/7',
      text: 'На связи с клиентами 24 часа в сутки, 7 дней в неделю',
    },
    {
      icon: 'mdi-cart-arrow-up',
      title: '30 дней на возврат',
      text: 'Простой возврат товара в течение 30 дней с даты покупки',
    },
    {
      icon: 'mdi-certificate-outline',
      title: 'Гарантия качества',
      text: 'Вся продукция имеет необходимые сертификаты',
    },

  ]


}
</script>
