<template>
    <header class="header">
      <nav>
        <ul class="menu">
          <li class="menu-item">
            <a href="#home" class="home">Home</a>
          </li>
          <li class="menu-item">
            <a href="#sobre-nos" class="sobre-nos">Sobre Nós</a>
          </li>
          <li class="menu-item">
            <a href="#servicos" class="servicos">Serviços</a>
          </li>
          <li class="menu-item">
            <a href="#contato" class="contato">Contato</a>
          </li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Header",
  };
  </script>
  
  <style scoped>
  /* Estilização geral do header */
  .header {
    width: 100%; /* Ajuste para largura responsiva */
    height: 85.4px;
    box-sizing: border-box;
  }
  
  /* Menu de navegação */
  nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
  }
  
  /* Lista de itens do menu */
  .menu {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    width: 80%;
    height: 100%;
    gap: 20px; /* Espaço entre os itens */
  }
  
  /* Itens individuais do menu */
  .menu-item {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid rgba(250, 239, 209, 1);
    border-radius: 30px;
    background-color: rgba(217, 217, 217, 0);
    height: 100%;
    padding: 12px;
    box-sizing: border-box;
  }
  
  /* Links dentro dos itens do menu */
  .menu-item a {
    text-decoration: none;
    color: rgba(0, 0, 0, 1);
    font-size: 40px;
    line-height: 100%;
    font-family: "Holtwood One SC", serif;
    font-weight: 400;
    text-align: center;
  }
  
  /* Ajustes individuais para cada item (se necessário) */
  .menu-item a:hover {
    color: rgba(250, 239, 209, 1); /* Cor ao passar o mouse */
    transition: color 0.3s ease;
  }
  </style>
  