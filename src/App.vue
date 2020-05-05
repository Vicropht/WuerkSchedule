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
        <v-stepper v-model="e1" dark>
          <v-stepper-header>
            <v-stepper-step :complete="e1 > 1" editable step="1">Input Weekly Hours</v-stepper-step>

            <v-divider></v-divider>

            <v-stepper-step :complete="e1 > 2" step="2">Set Hours</v-stepper-step>

            <v-divider></v-divider>

            <v-stepper-step step="3">Share</v-stepper-step>
          </v-stepper-header>

          <v-stepper-items>
            <v-stepper-content step="1">
              <v-card class="dark" max-width="400">
                <v-card-text>
                  <div>Hours in the week</div>
                  <p class="display-1">How many hours will you work this week?</p>
                  <input v-model.number="Hours" type="number">
                </v-card-text>
              </v-card>

              <v-btn color="primary" @click="e1 = 2">Continue</v-btn>
              <v-btn flat>Cancel</v-btn>
            </v-stepper-content>

            <v-stepper-content step="2">
              <v-card class="mb-5" color="grey lighten-1" height="200px"></v-card>

              <v-btn color="primary" @click="e1 = 3">Continue</v-btn>

              <v-btn flat>Cancel</v-btn>
            </v-stepper-content>

            <v-stepper-content step="3">
              <v-card class="mb-5" color="grey lighten-1" height="200px"></v-card>

              <v-btn color="primary" @click="e1 = 1">Continue</v-btn>

              <v-btn flat>Cancel</v-btn>
            </v-stepper-content>
          </v-stepper-items>
        </v-stepper>
      </v-layout>
    </v-content>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',

  components: {
    //
  },

  data: () => ({
    //
  }),
});
</script>
