<template>
  <v-card elevation="24" rounded="0" :color="color">
    <slot></slot>
  </v-card>
</template>
<script lang="ts">
import {Component, Prop, Vue} from "vue-property-decorator"
@Component
export default class CustomCard extends Vue {
  @Prop() color?: string
}
</script>
