<template>
    <div class="carousel-container" ref="carouselContainer">
      <div class="carousel-scroll" ref="carouselScroll" id="headline-scroll">
        <div v-for="(font, index) in fonts" :key="index" class="carousel-item">
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
          'Courier New, Courier, monospace',
          'Georgia, serif',
          'Times New Roman, Times, serif',
          'Verdana, Geneva, sans-serif',
          'Tahoma, Geneva, sans-serif',
          'Roboto, sans-serif',
          'Lobster, cursive',
        ]
      };
    },
    mounted() {
      this.cloneScrollContent();
    },
    methods: {
      cloneScrollContent() {
        // Clona o conteúdo para criar o efeito de rolagem contínua
        const headlineScroll = this.$refs.carouselScroll;
        const clone = headlineScroll.cloneNode(true);
        headlineScroll.parentNode.appendChild(clone);
  
        // Calcula a largura do conteúdo e aplica aos elementos
        const scrollWidth = headlineScroll.scrollWidth;
        headlineScroll.style.width = `${scrollWidth}px`;
        clone.style.width = `${scrollWidth}px`;
      },
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
    animation: scroll 15s linear infinite;
  }
  
  .carousel-item {
    flex: none;
    padding: 10px;
    display: inline-block;
    text-align: center;
  }
  
  .carousel-text {
    font-size: 30px;
    font-weight: bold;
    color: #333;
    transition: font-size 0.5s ease;
  }
  
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-100%);
    }
  }
  </style>
  