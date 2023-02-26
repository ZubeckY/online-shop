<template>
  <clean-card>
    <v-form>
      <v-container>
        <clean-card>
          <v-card-title class="pb-0">Всё ещё здесь?</v-card-title>
          <v-card-text>Подпишись на рассылку и будь вкурсе всех новинок на сайте</v-card-text>

          <v-card-actions class="ml-1" style="margin-top: -30px;">
            <v-text-field dense outlined
                          class="mt-6"
                          placeholder="Ваш email"/>
            <v-btn color="success"
                   class="text--lighten-2 ml-6 mt-0"
                   style="text-transform: none">Отправить</v-btn>
          </v-card-actions>

          <v-card-text style="margin-top: -40px">При подписке на рассылку, дарим 10% скидки на следующую покупку</v-card-text>
        </clean-card>
      </v-container>
    </v-form>
  </clean-card>
</template>

<script lang="ts">
import {Component, Vue} from "vue-property-decorator"
@Component
export default class MailingForm extends Vue {
}
</script>
