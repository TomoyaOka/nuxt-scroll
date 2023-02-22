<script setup lang="ts"></script>

<template>
  <div class="site-wrapper">
    <NuxtPage />
    <div class="contents-main">
      <div class="box" v-for="(item, index) in 20" :key="index">
        <img :src="`https://picsum.photos/1200/1000?random=${index}`" alt="" />
      </div>
    </div>
    <div class="main-bg"></div>
  </div>
</template>

<style lang="scss">
.site-wrapper {
  width: 100%;
  position: relative;
}

.main-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 0%;
  background-color: #fff;
  z-index: -1;
}

.contents-main {
  position: fixed;
  display: flex;
  flex-direction: column;
  gap: 30px;
  .box {
    width: 600px;
    height: 400px;
    filter: grayscale(100%);
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
}

@media (max-width: 768px) {
  .contents-main {
    .box {
      width: 200px;
      height: 150px;
    }
  }
}
</style>
