<template>
  <section id="contato">
    <div class="contact-container">
      <div class="left-side">
        <div class="posi-title">
          <h1 class="contact-title">Contate-nos</h1>
          <p class="subtitle">Alguma pergunta?<span> Nós mande um e-mail</span></p>
        </div>
        <div class="contact-info">
          <div class="info-item">
            <div class="icon-box">✉️</div>
            <div>
              <p class="info-title">Email</p>
              <p class="info-detail">contatodigitalprogressus@gmail.com</p>
            </div>
          </div>
          <div class="info-item">
            <div class="icon-box">📞</div>
            <div>
              <p class="info-title">Telefone</p>
              <p class="info-detail">+55 13 99686-4685</p>
            </div>
          </div>
          <div class="info-item">
            <a href="https://wa.me/5513996864685?text=Ol%C3%A1!%20Gostaria%20de%20saber%20mais%20sobre%20os%20servi%C3%A7os%20da%20Pr%C3%B3gressus."
              target="_blank" class="whatsapp-btn">
              💬 Fale no WhatsApp
            </a>

          </div>
        </div>
      </div>
      <!-- <div class="right-side">
        <form class="contact-form">
          <input type="text" placeholder="Seu nome" />
          <input type="email" placeholder="Seu E-mail" />
          <input type="text" placeholder="Seu título" />
          <textarea placeholder="Sua mensagem *"></textarea>
          <button type="submit">Envie uma Mensagem</button>
        </form>
      </div> -->
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Contact'
}
</script>

<style scoped>
.contact-container {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  min-height: 80vh;
  color: rgba(250, 239, 209, 1);
  padding: 20px 100px;
  align-items: center;
  justify-content: center;
}

.whatsapp-btn {
  display: inline-block;
  background-color: #25D366;
  color: white;
  padding: 12px 20px;
  border-radius: 25px;
  text-decoration: none;
  font-size: 16px;
  font-weight: bold;
  transition: background-color 0.3s ease;
  margin-top: 20px;
}

.whatsapp-btn:hover {
  background-color: #1ebe5d;
}

.posi-title {
  display: flex;
  flex-direction: column;
  text-align: center;
}

.left-side,
.right-side {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.contact-title {
  font-size: 40px;
  letter-spacing: 2px;
  font-weight: bold;
  color: #ff9400;
}

.subtitle {
  font-size: 20px;
  margin-top: 10px;
  color: rgba(250, 239, 209, 1);
}

.subtitle span {
  color: #ff9400;
}

.contact-info {
  margin-top: 50px;
}

.info-item {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.icon-box {
  width: 40px;
  height: 40px;
  background-color: #ff9400;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  margin-right: 15px;
  font-size: 20px;
  color: rgba(250, 239, 209, 1);
}

.info-title {
  font-size: 16px;
  color: #ff9400;
  margin-bottom: 5px;
}

.info-detail {
  font-size: 18px;
  color: rgba(250, 239, 209, 1);
}

.contact-form {
  width: 100%;
  max-width: 500px;
  display: flex;
  flex-direction: column;
}

.contact-form input,
.contact-form textarea {
  background-color: transparent;
  border: 1px solid #ff9400;
  padding: 15px 20px;
  margin-bottom: 20px;
  border-radius: 25px;
  color: rgba(250, 239, 209, 1);
  font-size: 16px;
  outline: none;
}

.contact-form textarea {
  min-height: 150px;
  resize: none;
}

.contact-form button {
  background: #ff9400;
  border: none;
  color: rgba(250, 239, 209, 1);
  padding: 15px;
  border-radius: 25px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s ease;
}

.contact-form button:hover {
  background-color: rgba(250, 239, 209, 1);
  color: #ff9400;
}

@media (max-width: 768px) {
  .contact-container {
    flex-direction: column;
    padding: 20px;
  }

  .left-side,
  .right-side {
    width: 100%;
    align-items: center;
    text-align: center;
  }

  .contact-title {
    font-size: 30px;
  }

  .subtitle {
    font-size: 18px;
  }

  .info-item {
    flex-direction: column;
    text-align: center;
  }

  .icon-box {
    margin-bottom: 10px;
  }

  .contact-form {
    width: 100%;
  }
}
</style>
