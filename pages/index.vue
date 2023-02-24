<template>
  <div>
    <v-card color="black"
            dark flat tile>
      <v-window v-model="onboarding">
        <v-window-item v-for="n in length"
                       :key="`card-${n}`">
          <v-card color="transparent" height="500">
            <v-row class="fill-height"
                   align="center" justify="center">
              <v-card-text class="text-center">
                Transparent themed, for background-imaged slides. Background color black added for demonstration purposes.
              </v-card-text>
            </v-row>
          </v-card>
        </v-window-item>
      </v-window>

      <v-card-actions class="justify-space-between">
        <v-btn text @click="prev">
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
        <v-item-group v-model="onboarding"
                      class="text-center" mandatory>
          <v-item v-for="n in length"
                  :key="`btn-${n}`"
                  v-slot="{ active, toggle }">
            <v-btn :input-value="active"
                   icon @click="toggle">
              <v-icon>mdi-record</v-icon>
            </v-btn>
          </v-item>
        </v-item-group>
        <v-btn text @click="next">
          <v-icon>mdi-chevron-right</v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>

    <v-card elevation="0" rounded="0">
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
    </v-card>

    <v-card elevation="0" rounded="0">

    </v-card>


    <v-form>
      <v-container>
        <v-card>

          <v-card-title class="pb-0">Всё ещё здесь?</v-card-title>
          <v-card-text>Подпишись на рассылку и будь вкурсе всех новинок на сайте</v-card-text>

          <v-row class="ml-1">
            <v-col cols="4">
              <v-text-field dense outlined
                            placeholder="Ваш email"/>
            </v-col>
            <v-col cols="2">
              <v-btn color="success"
                     class="text--lighten-2"
                     style="text-transform: none">Отправить</v-btn>
            </v-col>
          </v-row>

        </v-card>
      </v-container>
    </v-form>

  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Pages extends Vue {
  length:number = 6
  onboarding:number = 0

  next () {
    this.onboarding = this.onboarding + 1 === this.length ? 0 : this.onboarding + 1
  }

  prev () {
    this.onboarding = this.onboarding - 1 < 0 ? this.length - 1 : this.onboarding - 1
  }

}
</script>
