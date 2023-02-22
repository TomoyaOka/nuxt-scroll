<script setup lang="ts">
import Animation from "~~/assets/animation";

onMounted(() => {
  const app = new Animation();
  app.init();
});

/*----------------
* meta
------------------*/
useHead({
  title: "Index | Scroll ",
});
</script>

<template>
  <div class="index-page">
    <p><span id="js-count" data-from="0" data-num="100">0</span></p>
  </div>
</template>

<style lang="scss" scoped>
.index-page {
  position: fixed;
  top: 50%;
  right: 200px;
  transform: translateY(-50%);
  mix-blend-mode: difference;
  p {
    font-size: 300px;
    color: #fff;
    line-height: 0.95;
    overflow: hidden;
  }
  span {
    display: block;
    width: 200px;
    text-align: right;
  }
}

@media (max-width: 768px) {
  .index-page {
    position: fixed;
    top: 50%;
    right: 40px;

    p {
      font-size: 100px;
    }
    span {
      display: block;
      width: 100px;

      text-align: right;
    }
  }
}
</style>
