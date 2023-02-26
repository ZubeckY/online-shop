<template>
  <div>
    <v-footer color="grey" class="darken-4">
      <v-container>
        <v-row class="white--text" justify="center" no-gutters>

          <partials-footer-item-about/>
          <partials-footer-item-help/>
          <partials-footer-item-catalog/>
          <partials-footer-item-contact/>

        </v-row>
      </v-container>
    </v-footer>
  </div>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Footer extends Vue {
}
</script>
