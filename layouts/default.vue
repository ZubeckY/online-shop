<template>
  <v-app>
    <div style="background: #f3f3f3">
      <partials-header/>
      <nuxt/>
    </div>
  </v-app>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Default extends Vue {

}
</script>
