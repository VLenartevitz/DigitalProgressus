<template>
  <div class="footer">
    <div class="footer-content">

      <div class="secondContent">
        <div class="logo-container">
          <img :src="require('@/assets/images/Logo.png')" alt="Imagem local" class="logo" />
        </div>
        <div class="navigation">
          <p>Início</p>
          <p>Sobre Nós</p>
          <p>Serviços</p>
          <p>Contato</p>
        </div>

        <div class="social-media">
          <div class="icon-group">
            <div class="icon"></div>
            <p>Instagram</p>
          </div>
          <div class="icon-group">
            <div class="icon"></div>
            <p>Whats</p>
          </div>
          <div class="icon-group">
            <div class="icon"></div>
            <p>LinkedIn</p>
          </div>
        </div>
      </div>

      <div class="credits">
        <p>© 2024 Todos os direitos reservados.</p>
        <p>Desenvolvido por @VLenartevitz</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Footer",
};
</script>

<style scoped>
.footer {
  width: 100%;
  background-color: #ff9400;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 0;
}

.footer-content {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  gap: 30px;
}

.logo-container {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.logo {
  width: 120px;
  height: auto;
}

.secondContent {
  display: flex;
  justify-content: center; /* Centraliza o conteúdo */
  align-items: center;     /* Alinha os itens verticalmente */
  width: 100%;
  gap: 40px;
}

.navigation {
  flex: 1;
  display: flex;
  justify-content: center; /* Centraliza os itens dentro da navegação */
  align-items: center;
  flex-direction: column;
  gap: 20px;
  font-family: Archivo, sans-serif;
  font-weight: 700;
  font-size: 18px;
  color: black;
}

.social-media {
  flex: 1;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}

.icon-group {
  display: flex;
  flex-direction: row;
  align-items: center;
  font-family: Archivo, sans-serif;
  font-size: 14px;
  font-weight: 700;
  color: black;
}

.icon {
  width: 26px;
  height: 26px;
  background-color: black;
  border-radius: 50%;
  margin-right: 7px;
}

.credits {
  width: 100%;
  text-align: center;
  font-family: Archivo, sans-serif;
  font-size: 14px;
  font-weight: 700;
  margin-top: 20px;
  color: black;
}
</style>
