<template>
  <div class="about">
    <div class="text">这是一个设置页面</div>
    <div class="back" @click="back">
      <svg
        t="1605609350182"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="3252"
        width="20"
        height="20"
      >
        <path
          d="M438.4 297.6c12.8 12.8 12.8 28.8 3.2 41.6l-3.2 3.2L300.8 480H800c19.2 0 32 12.8 32 32 0 16-12.8 28.8-28.8 32H300.8l137.6 137.6c12.8 12.8 12.8 28.8 3.2 41.6l-3.2 3.2c-12.8 12.8-28.8 12.8-41.6 3.2l-3.2-3.2-192-192-3.2-3.2-3.2-3.2-3.2-3.2V499.2l3.2-3.2 3.2-3.2 3.2-3.2 192-192c12.8-12.8 32-12.8 44.8 0z"
          fill="#ffffff"
          p-id="3253"
        ></path>
      </svg>
    </div>
  </div>
</template>

<script>
import { Toast } from "vant";
export default {
  data() {
    return {
      adActive: false,
    };
  },
  methods: {
    back() {
      this.$router.back();
    },
  },
};
</script>

<style lang="less" scoped>
.about {
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  background: linear-gradient(#f6d365, #fda085);
  color: aliceblue;
  .text {
    margin: 40px;
  }
  .desc {
    font-weight: 700;
    font-size: 20px;
  }
  .back {
    position: absolute;
    left: 10px;
    top: 5px;
  }
  .ad-active {
    animation: rotate 1.5s linear;
  }

  @keyframes rotate {
    0% {
      transform: rotateZ(0deg); /*从0度开始*/
    }
    100% {
      transform: rotateZ(360deg); /*360度结束*/
    }
  }
}
</style>