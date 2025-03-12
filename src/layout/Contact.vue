<template>
    <div class="contact-container">
      <div class="background"></div>
      <h1 class="title">Contate-nos</h1>
      
      <div class="contact-item">
        <svg class="icon" width="66" height="66" viewBox="0 0 66 66" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M10.0588 3H24.1765L31.2353 20.6471L22.4118 25.9412C26.1916 33.6054 32.3946 39.8084 40.0588 43.5882L45.3529 34.7647L63 41.8235V55.9412C63 57.8133 62.2563 59.6087 60.9325 60.9325C59.6087 62.2563 57.8133 63 55.9412 63C42.1739 62.1634 29.1888 56.317 19.4359 46.5641C9.68296 36.8112 3.83665 23.8261 3 10.0588C3 8.18671 3.7437 6.39127 5.06748 5.06748C6.39127 3.7437 8.18671 3 10.0588 3Z" stroke="#FAEFD1" stroke-width="6" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <p class="text">number</p>
      </div>
  
      <div class="contact-item">
        <svg class="icon" width="78" height="62" viewBox="0 0 78 62" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 7.75C0 5.69457 0.821783 3.72333 2.28457 2.26992C3.74735 0.816515 5.73131 0 7.8 0H70.2C72.2687 0 74.2526 0.816515 75.7154 2.26992C77.1782 3.72333 78 5.69457 78 7.75V54.25C78 56.3054 77.1782 58.2767 75.7154 59.7301C74.2526 61.1835 72.2687 62 70.2 62H7.8C5.73131 62 3.74735 61.1835 2.28457 59.7301C0.821783 58.2767 0 56.3054 0 54.25V7.75ZM13.7241 7.75L39 29.7251L64.2759 7.75H13.7241ZM70.2 12.8999L41.5701 37.7929C40.8589 38.412 39.9456 38.7533 39 38.7533C38.0544 38.7533 37.1411 38.412 36.4299 37.7929L7.8 12.8999V54.25H70.2V12.8999Z" fill="#FAEFD1"/>
        </svg>
        <p class="text">email</p>
      </div>
      
      <p class="subtitle">Alguma pergunta? Nos mande um email</p>
      
      <div class="input-box"></div>
      <div class="input-box"></div>
      <div class="input-box textarea"></div>
      <div class="submit-button"></div>
    </div>
  </template>
  
  <script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Contact'
  }
  </script>
  
  <style scoped>
  .contact-container {
    width: 1440px;
    height: 954px;
    position: relative;
    background: black;
    padding: 20px;
    color: #FAEFD1;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .title {
    font-size: 80px;
    font-family: 'Holtwood One SC', serif;
    text-align: center;
  }
  
  .contact-item {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-top: 30px;
  }
  
  .icon {
    width: 66px;
    height: 66px;
  }
  
  .text {
    font-size: 40px;
    font-family: 'Gentium Book Plus', serif;
  }
  
  .subtitle {
    font-size: 30px;
    font-family: 'Gentium Book Plus', serif;
    margin-top: 50px;
  }
  
  .input-box {
    width: 438px;
    height: 75px;
    border-radius: 30px;
    border: 2px solid #FAEFD1;
    margin-top: 20px;
  }
  
  .textarea {
    height: 238px;
  }
  
  .submit-button {
    width: 320px;
    height: 71px;
    background: #FF0000;
    border-radius: 10px;
    margin-top: 30px;
  }
  </style>
  