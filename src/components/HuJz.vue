<script lang="ts">
import jzj1 from "./hujz/JZJ1.vue";
import $ from "jquery";

export default {
  data() {
    return {
      message: 'Hello World!',
      IDhujz: 'hu-jz',
      Classtrans: 'trans',
      Classjztou: 'jztou',
    }
  },
  components: {
    jzj1,
  }
}

</script>
<template>
  <div :id="IDhujz">
    <div :class="Classtrans">
      <span>加载中...</span>
    </div>
    <jzj1 />
  </div>
</template>

<style>
#hu-jz {
  position: fixed;
  z-index: 1000;
  width: 100%;
  height: 100%;
  display: flex;
  color: #94ff94;
  background-color: #76bcdf;
  justify-content: center;
  align-items: center;
  position: fixed;
}

.trans {
  position: absolute;
  width: 120px;
  height: 120px;
  /* 设置浮动 */
  display: flex;
  justify-content: center;
  align-items: center;
  background: #76bcdf;
}

span {
  position: absolute;
  color: #fff;
  z-index: 1;
}

.trans::after {
  content: "";
  position: absolute;
  width: 115px;
  height: 115px;
  background: #37474F;
  /* 添加边框 */
  border: 4px solid #3ff9dc;
  /* 初始化位置 */
  transform: rotate(45deg);
  /* 添加动画、动画时间和样式 */
  animation: rotate1 3s ease-in-out infinite alternate;
}

.trans::before {
  content: "";
  position: absolute;
  width: 115px;
  height: 115px;
  /* 添加边框 */
  border: 4px solid #ffab91;
  /* 初始化位置 */
  transform: rotate(-90deg);
  /* 添加动画、动画时间和样式 */
  animation: rotate2 3s ease-in-out infinite alternate;
}

@keyframes rotate1 {
  0% {
    transform: rotate(0deg);
  }

  25% {
    transform: rotate(-90deg);
  }

  50% {
    transform: rotate(-180deg);
  }

  75% {
    transform: rotate(-270deg);
  }

  100% {
    transform: rotate(-360deg);
  }
}

@keyframes rotate2 {
  0% {
    transform: rotate(0deg);
  }

  25% {
    transform: rotate(90deg);
  }

  50% {
    transform: rotate(180deg);
  }

  75% {
    transform: rotate(270deg);
  }

  100% {
    transform: rotate(360deg);
  }
}
</style>