<script lang="ts">
import $ from "jquery";

export default {
  data() {
    return {
      IDprogress: 'fileProgress',
      IDBar: 'fileBar',
    }
  }
}

var IDBar = document.getElementById("fileBar");
var jdt = 0;
var timer = setInterval(function () {
  console.log(jdt)
  // IDBar.style.width = num + "%";
  // IDBar.innerText = num + "%";
  $("#fileBar").css("width", jdt + "%").text(jdt + '%');  //jquery 实现
  if (jdt == 100) {
    console.log("进度条100%了！")
    $('#fileBar').css('color' , 'gold').text('lemonhu & 狐窝')
    console.log('欢迎来到 柠檬狐的狐窝')
    $('#hu-jz').toggle().css('display','none')
    console.log('加载完成，已隐藏加载')
    clearInterval(timer);
  } else {
    jdt += 10;
  }
}, 1000);
</script>
<template>
  <div :id="IDprogress">
    <div :id="IDBar">0%</div>
  </div>
</template>
<style>
#fileProgress {
  position: fixed;
  top: 70%;
  width: 20%;
  background-color: #e2e2e2;
  border-radius: 10px;
}

#fileBar {
  width: 0;
  height: 20px;
  line-height: 20px;
  background-color: #5FB878;
  text-align: center;
  color: white;
  border-radius: 10px;
}
</style>