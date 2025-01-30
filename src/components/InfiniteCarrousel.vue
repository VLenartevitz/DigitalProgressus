<template>
  <div class="carousel-container" ref="carouselContainer">
    <div class="carousel-scroll" ref="carouselScroll">
      <div v-for="(font, index) in fonts" :key="index" class="carousel-item">
        <p class="carousel-text" :style="{ fontFamily: font }">Sobre Nós</p>
      </div>
      <div v-for="(font, index) in fonts" :key="`clone-${index}`" class="carousel-item">
        <p class="carousel-text" :style="{ fontFamily: font }">Sobre Nós</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfiniteCarousel',
  data() {
    return {
      fonts: [
        'Arial, sans-serif',
        'Times New Roman, Times, serif',
        'Courier New, Courier, monospace',
        'Georgia, serif',
        'Roboto, sans-serif',
        'Tahoma, Geneva, sans-serif',
        'Lobster, cursive',
      ],
    };
  },
};
</script>

<style scoped>
.carousel-container {
  width: 100%;
  overflow: hidden;
  position: relative;
}

.carousel-scroll {
  display: flex;
  flex-wrap: nowrap;
  animation: scroll 20s linear infinite;
}

.carousel-item {
  flex: none;
  padding: 20px;
  display: inline-block;
  text-align: center;
}

.carousel-text {
  font-size: 50px;
  font-weight: bold;
  color: #ffffff;
  transition: font-size 0.5s ease;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%); /* Move apenas metade do conteúdo */
  }
}
</style>