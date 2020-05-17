<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <h2>Wuerk Scheduler</h2>
      </div>
      <v-spacer></v-spacer>
      <v-btn href="https://github.com/Vicropht/WuerkSchedule" target="_blank" text>
        <span class="mr-2">GITHUB REPO</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-layout align-center justify-center column fill-height>
        <input-hours />
      </v-layout>
    </v-content>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import InputHours from './components/InputHours.vue';

export default Vue.extend({
  name: 'App',

  components: {
    InputHours,
  },

  data: () => ({
    return: {
      e1: 0,
    },
  }),
});
</script>
