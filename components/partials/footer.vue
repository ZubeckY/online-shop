<template>
  <v-footer color="grey" class="darken-4">
    <v-container>
      <v-row class="white--text" justify="center" no-gutters>

        <v-col>
          <div class="text-h6 white--text">О компании</div>

          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
        </v-col>

        <v-col>
          <div class="text-h6 white--text">Помощь</div>

          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Где мой заказ?</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Доставка и оплата</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Гарантии и возврат</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Подарочные сертификаты</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Бонусная программа</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Рассрочка и кредит</v-btn>
          </div>
        </v-col>

        <v-col>
          <div class="text-h6 white--text">Каталог</div>
          
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
          <div>
            <v-btn class="pa-0" color="grey" text
                   style="text-transform: none">Кнопка</v-btn>
          </div>
        </v-col>

        <v-col>
          <div class="text-h6">8 800 888-88-88</div>
          <div>с 9:00 до 22:00, без выходных</div>

          <v-btn icon>
            <svg version="1.0" xmlns="http://www.w3.org/2000/svg"
                 width="16.000000pt" height="16.000000pt" viewBox="0 0 16.000000 16.000000"
                 preserveAspectRatio="xMidYMid meet">

              <g transform="translate(0.000000,16.000000) scale(0.100000,-0.100000)" stroke="none" fill="#fff">
                <path d="M4 116 c-3 -8 -4 -29 -2 -48 l3 -33 75 0 75 0 0 45 0 45 -73 3 c-56
                        2 -74 0 -78 -12z m86 -26 c13 -9 13 -11 0 -20 -22 -15 -30 -12 -30 10 0 22 8
                        25 30 10z"/>
              </g>
            </svg>
          </v-btn>

          <v-btn icon>
            <svg version="1.0" xmlns="http://www.w3.org/2000/svg"
                 width="16.000000pt" height="16.000000pt" viewBox="0 0 16.000000 16.000000"
                 preserveAspectRatio="xMidYMid meet">

              <g transform="translate(0.000000,16.000000) scale(0.100000,-0.100000)" stroke="none" fill="#fff">
                <path d="M0 114 c0 -18 62 -84 79 -84 6 0 11 7 11 15 0 8 4 15 9 15 5 0 14 -7
                        21 -15 14 -16 40 -20 40 -6 0 5 -6 14 -14 21 -12 9 -13 17 -4 36 15 32 0 45
                        -19 17 -19 -28 -33 -29 -33 -3 0 31 -28 24 -32 -7 l-4 -28 -14 28 c-14 29 -40
                        37 -40 11z"/>
              </g>
            </svg>
          </v-btn>

          <v-btn icon>
            <svg version="1.0" xmlns="http://www.w3.org/2000/svg"
                 width="16.000000pt" height="16.000000pt" viewBox="0 0 16.000000 16.000000"
                 preserveAspectRatio="xMidYMid meet">

              <g transform="translate(0.000000,16.000000) scale(0.100000,-0.100000)" stroke="none" fill="#fff">
                <path d="M78 121 c-80 -32 -86 -37 -59 -46 13 -4 37 3 68 20 l48 27 -35 -31
                        -35 -31 28 -25 c16 -14 32 -23 36 -20 5 2 11 24 15 47 4 24 9 53 13 66 6 27 5
                        27 -79 -7z"/>
              </g>
            </svg>
          </v-btn>

        </v-col>

      </v-row>
    </v-container>
  </v-footer>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Footer extends Vue {
}
</script>
