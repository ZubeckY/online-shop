<template>
  <v-app>
    <div style="background: #f3f3f3; min-height: 100vh;">
      <partials-header/>
      <nuxt/>
      <partials-footer/>
    </div>
  </v-app>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Default extends Vue {

}
</script>
