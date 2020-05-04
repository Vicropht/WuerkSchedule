<template>
  <body>
    <img alt="Clock" src="../assets/clock.png">
    <p> How many hours are you working this week?</p>
    <input v-model="message" placeholder="(Total time in hours)">
    </body>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class InputHours extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

img {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  box-shadow: 0 0 1em black;
}
</style>
