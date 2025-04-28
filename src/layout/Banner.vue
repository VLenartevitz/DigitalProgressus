<template>
  <section id="home">
  <div class="banner">
    <div class="content-wrapper">
      <div class="text-container">
        <h1 class="title">PRÓGRESSUS</h1>
        <h2 class="subtitle">A TRANSFORMAÇÃO COMEÇA AGORA</h2>
      </div>
      <img src="../assets/images/LOGO P - PNG.png" class="logo" />
    </div>
  </div>
</section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Banner'
}
</script>

<style scoped>
.banner {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: #000000;
  color: white;
  animation: fadeIn 1.5s ease-in-out;
  padding: 20px;
  box-sizing: border-box;
}

.content-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 80px;
  width: 90%;
  max-width: 1400px;
}

.text-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.logo {
  width: 800px;
  height: auto;
  animation: slideIn 1s ease-in-out;
}

.title {
  font-size: 100px;
  font-weight: bold;
  margin: 0;
  padding: 0;
  /* font-family: 'Arial', sans-serif; */
  text-transform: uppercase;
  letter-spacing: 5px;
  line-height: 1;
}

.subtitle {
  font-size: 36px;
  margin-top: 20px;
  animation: fadeIn 1.5s ease-in-out;
  /* font-family: 'Arial', sans-serif; */
  font-weight: normal;
  letter-spacing: 3px;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideIn {
  from {
    transform: translateY(-30px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

/* Responsividade */

@media (max-width: 1200px) {
  .content-wrapper {
    flex-direction: column;
    gap: 40px;
  }
  
  .text-container {
    align-items: center;
    text-align: center;
  }
  
  .logo {
    width: 600px;
  }
  
  .title {
    font-size: 80px;
  }
  
  .subtitle {
    font-size: 28px;
  }
}

@media (max-width: 992px) {
  .logo {
    width: 500px;
  }
  
  .title {
    font-size: 60px;
  }
  
  .subtitle {
    font-size: 24px;
  }
}

@media (max-width: 768px) {
  .logo {
    width: 400px;
  }
  
  .title {
    font-size: 50px;
  }
  
  .subtitle {
    font-size: 20px;
  }
}

@media (max-width: 576px) {
  .content-wrapper {
    gap: 20px;
  }
  
  .logo {
    width: 300px;
  }
  
  .title {
    font-size: 10px;
  }
  
  .subtitle {
    font-size: 18px;
  }
}
</style>