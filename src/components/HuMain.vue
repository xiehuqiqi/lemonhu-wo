<script lang="ts">
import $ from "jquery";

export default {
  data() {
    return {
      IDmain: 'main',
      IDnav: 'dhnav',
      Classnavtou: 'nav-tou',
    }
  }
}
</script>
<template>
  <div :id="IDmain">
    <nav :id="IDnav">
      <ul>
        <li>
          hhh
        </li>
      </ul>
      <ul>
        <li>
          
        </li>
      </ul>
      
    </nav>
  </div>
</template>
<style>
#main {
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

#dhnav {
  position: relative;
  z-index: 1000;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 50px;
  background-color: rgb(58, 212, 78);
  border-radius: 20px 20px 20px 20px;
}

.nav-tou {
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;

}
</style>