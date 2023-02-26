<template>
  <v-app>
    <div class="d-flex flex-column" style="background: #f3f3f3; min-height: 100vh;">
      <partials-header/>

      <div style="flex: 1 0 auto;">
        <nuxt/>
      </div>

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
