<template>
  <header class="header">
    <nav>
      <ul class="menu">
        <li class="menu-item"> 
          <a href="#home" class="nav-link">Home</a>
        </li>
        <li class="menu-item">
          <a href="#sobre-nos" class="nav-link">Sobre Nós</a>
        </li>
        <li class="menu-item">
          <a href="#servicos" class="nav-link">Serviços</a>
        </li>
        <li class="menu-item">
          <a href="#contato" class="nav-link">Contato</a>
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
  height: 85.4px;
  padding-top: 30px;
  background-color: #000000;
  position: relative;
  z-index: 100;
}

/* Menu principal */
.menu {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0 auto;
  width: 80%;
  height: 100%;
  gap: 20px;
}

/* Itens do menu */
.menu-item {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid rgba(250, 239, 209, 1);
  border-radius: 30px;
  height: 100%;
  padding: 12px;
  box-sizing: border-box;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
  transform-style: preserve-3d;
  position: relative;
  overflow: hidden;
}

/* Efeito hover completo */
.menu-item:hover {
  border-color: #ff9400;
  box-shadow: 0 0 15px rgba(255, 148, 0, 0.6);
  transform: translateY(-3px);
}

/* Links de navegação */
.nav-link {
  text-decoration: none;
  color: rgba(250, 239, 209, 1);
  font-size: 40px;
  font-family: "Holtwood One SC", serif;
  transition: all 0.4s ease;
  display: block;
  width: 100%;
  text-align: center;
}

/* Animação do link */
.menu-item:hover .nav-link {
  color: #ff9400;
  transform: scale(1.05);
  text-shadow: 0 0 8px rgba(255, 148, 0, 0.4);
}

/* Efeito de "pulse" sutil */
@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.02); }
  100% { transform: scale(1); }
}

.menu-item {
  animation: pulse 6s infinite;
}

.menu-item:hover {
  animation: none;
}

/* Responsivo */
@media (max-width: 1200px) {
  .menu { width: 95%; gap: 10px; }
  .nav-link { font-size: 30px; }
}

@media (max-width: 768px) {
  .menu { flex-direction: column; height: auto; gap: 15px; }
  .menu-item { width: 90%; height: 60px; }
  .nav-link { font-size: 24px; }
}
</style>