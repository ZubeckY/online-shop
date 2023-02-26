<template>
  <v-col>
    <div class="text-h6">8 800 888-88-88</div>
    <div>с 9:00 до 22:00, без выходных</div>
    <v-btn icon>
      <partials-footer-icon-yt/>
    </v-btn>
    <v-btn icon>
      <partials-footer-icon-vk/>
    </v-btn>
    <v-btn icon>
      <partials-footer-icon-tg/>
    </v-btn>
  </v-col>
</template>
<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class Contact extends Vue {
}
</script>
