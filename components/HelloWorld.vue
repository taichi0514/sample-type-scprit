<template>
  <ul>
    <li>{{message}}</li>
    <li>{{number}}</li>
    <li>{{title}}</li>
    <li>{{description}}</li>
    <li>{{typo}}</li>
    <label for>
      <input v-model="meg">
      <button @click="onClick(meg)">change</button>
    </label>
  </ul>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";
@Component
export default class HelloWorld extends Vue {
  @Prop({ type: String })
  message: string = "Hello world !";
  number: number = 514;
  title: string = "wifi";
  description: string = "説明";
  typo: string = "タイポじゃ";
  onClick(text) {
    this.message = text;
  }
}
</script>
