<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="6">
        <v-text-field
          readonly
          prepend-icon="mdi-message-text-outline"
          v-model="messageToSend"
          label="System ID"
        ></v-text-field>
      </v-col>

      <v-col cols="2" class="row-btn">
        <v-btn color="grey darken-4" @click="sendMessages">Send message</v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue';
import { EventBus, LicenseEvent } from '@/utility/eventBus';

export default Vue.extend({
  name: 'Asconfig',
  data(): {
    signing: boolean;
  } {
    return {
      signing: false,
    };
  },
});
</script>

<style lang="scss" scoped>
.upload-btn {
  display: flex;
  margin-top: 15px;
  align-items: center;
}

.row-btn {
  display: flex;
  margin-top: 0px;
  align-items: center;
}

.mini-row {
  height: 40px;
}
</style>
