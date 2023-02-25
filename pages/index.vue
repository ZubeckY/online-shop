<template>
  <div>
    <v-carousel cycle height="600"
                hide-delimiter-background
                show-arrows-on-hover>
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-sheet :color="slide.color"
                 height="100%">
          <v-row class="fill-height ma-0"
                 align="center"
                 justify="center">
            <v-container>
              <div class="text-center text-h2">
                {{ slide.text }} Slide
              </div>
            </v-container>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>

    <clean-card>
      <v-container>
        <v-row class="pt-3">
          <v-col class="text-center">
            <v-icon color="success" class="text--lighten-2" style="font-size: 45px">mdi-truck-fast-outline</v-icon>
            <v-card-title class="justify-center pb-0" style="font-size: 16px">Бесплатная доставка</v-card-title>
            <v-card-text style="font-size: 12px">Бесплатная доставка по России при сумме заказа от 3000 руб.</v-card-text>
          </v-col>

          <v-col class="text-center">
            <v-icon color="success" class="text--lighten-2" style="font-size: 45px">mdi-clock-fast</v-icon>
            <v-card-title class="justify-center pb-0" style="font-size: 16px">Поддержка 24/7</v-card-title>
            <v-card-text style="font-size: 12px">На связи с клиентами 24 часа в сутки, 7 дней в неделю</v-card-text>
          </v-col>

          <v-col class="text-center">
            <v-icon color="success" class="text--lighten-2" style="font-size: 45px">mdi-cart-arrow-up</v-icon>
            <v-card-title class="justify-center pb-0" style="font-size: 16px">30 дней на возврат</v-card-title>
            <v-card-text style="font-size: 12px">Простой возврат товара в течение 30 дней с даты покупки</v-card-text>
          </v-col>

          <v-col class="text-center">
            <v-icon color="success" class="text--lighten-2" style="font-size: 45px">mdi-certificate-outline</v-icon>
            <v-card-title class="justify-center pb-0" style="font-size: 16px">Гарантия качества</v-card-title>
            <v-card-text style="font-size: 12px">Вся продукция имеет необходимые сертификаты</v-card-text>
          </v-col>
        </v-row>
      </v-container>
    </clean-card>

    <clean-card>

    </clean-card>

    <v-form>
      <v-container>
        <clean-card>
          <clean-card class="mx-auto" style="max-width: 600px">
            <v-card-title class="pb-0">Всё ещё здесь?</v-card-title>
            <v-card-text>Подпишись на рассылку и будь вкурсе всех новинок на сайте</v-card-text>

            <v-card-actions class="ml-1" style="margin-top: -30px;">
              <v-text-field dense outlined
                            class="mt-6"
                            placeholder="Ваш email"/>
              <v-btn color="success"
                     class="text--lighten-2 ml-6 mt-0"
                     style="text-transform: none">Отправить</v-btn>
            </v-card-actions>

            <v-card-text style="margin-top: -40px">При подписке на рассылку, дарим 10% скидки на следующую покупку</v-card-text>
          </clean-card>
        </clean-card>
      </v-container>
    </v-form>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Pages extends Vue {

  slides:any = [
    {
      color: 'indigo',
      text: 'First'
    },
    {
      color: 'warning',
      text: 'Second'
    },
    {
      color: 'pink darken-2',
      text: 'Third'
    },
    {
      color: 'red lighten-1',
      text: 'Fourth'
    },
    {
      color: 'deep-purple accent-4',
      text: 'Fifth'
    },
  ]

}
</script>
