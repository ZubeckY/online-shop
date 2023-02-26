<template>
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
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"

@Component
export default class Slider extends Vue {
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
