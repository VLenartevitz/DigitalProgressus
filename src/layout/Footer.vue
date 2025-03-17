<template>
  <div class="footer">
    <div class="footer-content">

      <div class="secondContent">
        <!-- Logo -->
        <div class="logo-container">
          <img :src="require('@/assets/images/Logo.png')" alt="Logo da empresa" class="logo" />
        </div>

        <!-- Navegação -->
        <div class="navigation">
          <p @click="navigate('inicio')">Início</p>
          <p @click="navigate('sobre')">Sobre Nós</p>
          <p @click="navigate('servicos')">Serviços</p>
          <p @click="navigate('contato')">Contato</p>
        </div>

        <!-- Redes sociais -->
        <div class="social-media">
          <a href="https://www.instagram.com" target="_blank" aria-label="Instagram" class="icon-group">
            <i class="fab fa-instagram icon"></i>
            <p>Instagram</p>
          </a>
          <a href="https://wa.me/1234567890" target="_blank" aria-label="WhatsApp" class="icon-group">
            <i class="fab fa-whatsapp icon"></i>
            <p>WhatsApp</p>
          </a>
          <a href="https://www.linkedin.com" target="_blank" aria-label="LinkedIn" class="icon-group">
            <i class="fab fa-linkedin icon"></i>
            <p>LinkedIn</p>
          </a>
        </div>
      </div>

      <!-- Créditos -->
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
  methods: {
    navigate(section) {
      // Exemplo de navegação: pode integrar com Vue Router
      console.log(`Ir para ${section}`);
    }
  }
};
</script>

<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

.footer {
  width: 100%;
  background-color: #e67e22;
  /* Laranja queimado */
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 60px 0;
  /* Aumentei o padding */
  color: #000;
  /* Texto preto */
}

.footer-content {
  width: 100%;
  max-width: 1200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  /* Aumentei o espaçamento */
}

.secondContent {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: flex-start;
  gap: 100px;
  /* Mais espaço entre as seções */
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  width: 120px;
  height: auto;
}

/* Navegação */
.navigation {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  /* Maior espaçamento */
  font-family: Archivo, sans-serif;
  font-weight: 700;
  font-size: 18px;
  color: #000;
  /* Letras pretas */
}

.navigation p {
  cursor: pointer;
  transition: all 0.3s ease;
}

.navigation p:hover {
  color: #333;
  /* Cinza escuro para hover */
  transform: translateY(-2px);
}

/* Redes sociais */
.social-media {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 25px;
  /* Mais espaço entre os itens */
}

.icon-group {
  display: flex;
  align-items: center;
  gap: 10px;
  color: #000;
  /* Letras pretas */
  font-family: Archivo, sans-serif;
  font-size: 16px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
}

.icon-group:hover {
  transform: translateY(-2px);
}

.icon {
  font-size: 26px;
  color: #000;
  /* Ícones pretos */
}

/* Créditos */
.credits {
  width: 100%;
  text-align: center;
  font-family: Archivo, sans-serif;
  font-size: 14px;
  font-weight: 400;
  padding-top: 30px;
  /* Mais espaço antes do crédito */
  border-top: 1px solid rgba(0, 0, 0, 0.2);
  /* Linha de separação mais visível */
  color: #000;
  /* Texto preto */
}

/* Responsividade */
@media (max-width: 768px) {
  .secondContent {
    flex-direction: column;
    align-items: center;
    gap: 40px;
    /* Mantendo espaçamento bom no mobile */
  }

  .navigation,
  .social-media {
    align-items: center;
  }
}
</style>
