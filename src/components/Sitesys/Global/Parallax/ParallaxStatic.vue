<template>
  <div
    class="parallax--image"
    :style="{
      backgroundImage: `url(${image})`,
      height: size,
      backgroundAttachment: attachment,
    }"
  >
    <div
      :style="{
        width: '100%',
        backgroundColor: color,
        opacity: opacity,
      }"
    />
    <div class="parallax--container">
      <slot name="title" />
    </div>
    <div class="parallax--container1">
      <slot name="subtitle" />
    </div>
    <div class="parallax--default">
      <slot name="default" />
    </div>
  </div>
</template>

<script setup>
import imgUrl from '@/assets/images/sitesys/parallax/parallax-01.png'

defineProps({
  image: {
    type: String,
    default: imgUrl, // Random image "https://placeimg.com/500/300/nature?t=" + Math.random()
  },
  size: {
    type: String,
    default: '60vh',
  },
  color: {
    type: String,
    default: '#1D1D1D',
  },
  opacity: {
    type: Number,
    default: 0.1,
  },
  attachment: {
    type: String,
    default: 'fixed',
  },
})
</script>

<style lang="scss" scoped>
.parallax--image {
  overflow: hidden;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  display: flex;
  position: relative;
  background-attachment: fixed;
}
.parallax--container {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  overflow: hidden;
}
.parallax--container1 {
  position: absolute;
  top: 90%;
  left: 50%;
  transform: translate(-50%, -50%);
  overflow: hidden;
}

.parallax--default {
  position: absolute;
  overflow: hidden;
}
</style>
