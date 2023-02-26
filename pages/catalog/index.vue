<template>
  <v-container>
    <v-breadcrumbs :items="items" divider="-"></v-breadcrumbs>
    <v-row>
      <v-col cols="3">
        <clean-card>
          <v-card-title class="py-2">Фильтры</v-card-title>

          <!-- -->
          <v-card-text class="py-0">Сортировать по</v-card-text>
          <v-card-text class="pt-0">
            <v-select :items="sortOne" hide-details
                      outlined dense></v-select>
          </v-card-text>

          <!-- -->
          <v-card-text class="py-0">Сортировать по</v-card-text>
          <v-card-text class="pt-0">
            <v-select :items="sortTwo" hide-details
                      outlined dense></v-select>
          </v-card-text>

          <!-- -->
          <v-card-text class="py-0">Категория</v-card-text>
          <v-card-text class="pt-0">
            <v-select :items="categories" hide-details
                      outlined dense></v-select>
          </v-card-text>

          <!-- -->
          <v-card-text class="pt-0">Наличие</v-card-text>
          <v-card-text class="py-0">
            <v-checkbox class="ma-0 pa-0" label="В наличии"></v-checkbox>
            <v-checkbox class="ma-0 pa-0" label="Под Заказ"></v-checkbox>
          </v-card-text>

          <!-- -->
          <v-card-text class="pt-0">Категории</v-card-text>
          <v-card-text class="py-0">
            <v-checkbox class="ma-0 pa-0" label="Скидка"></v-checkbox>
            <v-checkbox class="ma-0 pa-0" label="Хит"></v-checkbox>
          </v-card-text>

          <!-- -->
          <v-card-text class="py-0">Цена</v-card-text>
          <v-card-text class="pt-0">
            <v-row>
              <v-col class="px-4">
                <v-range-slider v-model="range"
                                hide-details
                                class="align-center"
                                track-color="#cfcfcf"
                                :max="max" :min="min">
                </v-range-slider>
                <v-row>
                  <v-col cols="auto">
                    <v-text-field :value="range[0]"
                                  class="mt-0 pt-0"
                                  hide-details
                                  outlined dense
                                  type="number"
                                  style="width: 90px"
                                  @change="$set(range, 0, $event)"></v-text-field>
                  </v-col>
                  <v-spacer/>
                  <v-col cols="auto">
                    <v-text-field :value="range[1]"
                                  class="mt-0 pt-0"
                                  hide-details
                                  outlined dense
                                  type="number"
                                  style="width: 90px"
                                  @change="$set(range, 1, $event)"></v-text-field>
                  </v-col>
                </v-row>

              </v-col>
            </v-row>
          </v-card-text>

        </clean-card>
      </v-col>

      <v-col cols="9">
        <div class="d-flex flex-row flex-wrap">
          <catalog-card v-for="i in itemsPerPage" :key="i"></catalog-card>
        </div>

        <div class="text-center">
          <v-pagination v-model="page"
                        :length="pageCount"
                        :total-visible="7"
                        prev-icon="mdi-menu-left"
                        next-icon="mdi-menu-right">
          </v-pagination>
        </div>
      </v-col>

    </v-row>
  </v-container>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"

@Component
export default class Catalog extends Vue {
  page:number = 1
  pageCount:number = 2
  itemsPerPage:number = 9


  min:number = 100
  max:number = 10000
  range:number[] = [100, 10000]

  sortOne = [
    {
      text: 'Название', value: 'title'
    },
    {
      text: 'Цена', value: 'price'
    }
  ]
  sortTwo = [
    {
      text: 'Возрастанию А-я', value: 'Asc'
    },
    {
      text: 'Убыванию Я-а', value: 'Desc'
    }
  ]
  categories = [
    {
      text: 'Мыло', value: 'soap'
    },
    {
      text: 'Жидкое мыло', value: 'liquid_soap'
    }
  ]

  items = [
    {
      text: 'Главная',
      disabled: false,
      href: '/',
    },
    {
      text: 'Каталог',
      disabled: false,
      href: '/catalog',
    }
  ]
}
</script>
