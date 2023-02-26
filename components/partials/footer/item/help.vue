<template>
  <v-col>
    <div class="text-h6 white--text">Помощь</div>
    <div v-for="(item, i) in help" :key="i">
      <v-btn class="pa-0" color="grey" text
             @click="routing(item.link)"
             style="text-transform: none">{{item.text}}</v-btn>
    </div>
  </v-col>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Help extends Vue {
  help = [
    {
      link: '/',
      text: 'Где мой заказ?'
    },
    {
      link: '/',
      text: 'Доставка и оплата'
    },
    {
      link: '/',
      text: 'Гарантии и возврат'
    },
    {
      link: '/',
      text: 'Подарочные сертификаты'
    },
    {
      link: '/',
      text: 'Бонусная программа'
    },
    {
      link: '/',
      text: 'Рассрочка и кредит'
    },
  ]

  routing (link:string) {
    this.$router.push(link)
  }
}
</script>
