<template>
  <header class="header">
    <nav>
      <ul class="menu">
        <li>
          <a href="#home" class="menu-item nav-link">Home</a>
        </li>
        <li>
          <a href="#sobre-nos" class="menu-item nav-link">Sobre Nós</a>
        </li>
        <li>
          <a href="#servicos" class="menu-item nav-link">Serviços</a>
        </li>
        <li>
          <a href="#contato" class="menu-item nav-link">Contato</a>
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
/* Estilização geral */
.header {
  width: 100%;
  height: auto;
  padding: 20px 0;
  background-color: #000000;
  position: relative;
  z-index: 100;
}

/* Menu principal */
.menu {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0 auto;
  width: 90%;
  gap: 15px;
}

/* Itens do menu */
.menu-item {
  /* Tudo igual como já está */
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid rgba(250, 239, 209, 1);
  border-radius: 30px;
  padding: 20px 30px; /* Aumenta a área clicável */
  box-sizing: border-box;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
  position: relative;
  overflow: hidden;
  min-width: 120px;
  text-decoration: none; /* Já evita sublinhado */
  color: rgba(250, 239, 209, 1);
  font-size: 24px;
  text-align: center;
}

.menu-item:hover {
  border-color: #ff9400;
  box-shadow: 0 0 15px rgba(255, 148, 0, 0.6);
  transform: translateY(-3px);
  color: #ff9400;
  text-shadow: 0 0 8px rgba(255, 148, 0, 0.4);
}


/* Links de navegação */
.nav-link {
  text-decoration: none;
  color: rgba(250, 239, 209, 1);
  font-size: 24px;
  /* font-family: "Holtwood One SC", serif; */
  transition: all 0.4s ease;
  text-align: center;
  display: block;
}

.menu-item:hover .nav-link {
  color: #ff9400;
  transform: scale(1.05);
  text-shadow: 0 0 8px rgba(255, 148, 0, 0.4);
}

/* Responsivo */
@media (max-width: 1024px) {
  .menu { width: 100%; gap: 10px; }
  .nav-link { font-size: 20px; }
}

@media (max-width: 768px) {
  .menu {
    flex-direction: column;
    width: 100%;
  }
  .menu-item {
    width: 80%;
    padding: 10px;
  }
  .nav-link { font-size: 18px; }
}
</style>
