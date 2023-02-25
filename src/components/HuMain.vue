<script lang="ts">
import $ from "jquery";

export default{
  data () {
    return {
      IDmain : 'main',
    }
  }
}
</script>
<template>
  <div :id="IDmain">
    <h1>222</h1>
  </div>
</template>
<style>
#main{
  position: fixed;
  z-index: 1;
  top: 0px;
  left: 0px;
  z-index: 100;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.548);
  /* justify-content: center;
  align-items: center; */
}
</style>