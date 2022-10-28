<template>
  <h4>Type Story:-</h4>
  <textarea name="" id="" cols="50" rows="4" v-model.lazy="text"></textarea>
  <div class="parent">
  <div><h4>Type color</h4> <input type="text" v-model.lazy="color" name="" id=""></div>
  <div><h4>Type background-color</h4> <input type="text" v-model.lazy="bgcolor" name="" id=""></div>
  <div><h4>Type height</h4> <input type="text" v-model="height" name="" id=""></div>
  <div><h4>Type width</h4> <input type="text" v-model="width" name="" id=""></div>
  <div><h4>Type padding</h4> <input type="text" v-model="padding" name="" id=""></div></div>
  <div class="box">{{text.toUpperCase()}}</div>
</template>
<script lang="ts">
import { ref } from "vue";

export default {
  name: "StyleBox",
  setup() {
    const text  = ref<string>("");
    const color = ref<string>("");
    const bgcolor = ref<string>("");
const height = ref<string>("");
const width = ref<string>("");
const padding = ref<string>("");
     return {
      text,
      color,
      bgcolor,
      height,
      width,
      padding
    };
  },
};
</script>
<style>
.box{
    text-align: center;
    margin: auto;
 color: v-bind(color);
 background-color: v-bind(bgcolor);
 height: v-bind(height);
 width:v-bind(width);
 padding: v-bind(padding);
 margin-bottom: 100px;
 border-radius: 15px;
 font-weight: 900;
 font-size: 23px;
 font-family:"system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif";

}
.parent{
    display: flex;
    gap: 60px;
    padding: 15px;
}
</style>