<template>
  <v-col>
    <div class="text-h6 white--text">Каталог</div>
    <div v-for="(item, i) in catalog" :key="i">
      <v-btn class="pa-0" color="grey" text
             @click="routing(item.link)"
             style="text-transform: none">{{item.text}}</v-btn>
    </div>
  </v-col>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Catalog extends Vue {
  catalog = [
    {
      link: '/',
      text: 'Кнопка'
    },
    {
      link: '/',
      text: 'Кнопка'
    },
    {
      link: '/',
      text: 'Кнопка'
    }
  ]

  routing (link:string) {
    this.$router.push(link)
  }
}
</script>
