<template>
  <div class="contact-container">
    <div class="left-side">

      <div class="posi-title">
      <h1 class="contact-title">CONTACT ME</h1>
      <p class="subtitle">LET'S <span>Talk About Ideas</span></p>
    </div>

      <div class="contact-info">
        <div class="info-item">
          <div class="icon-box">🏠</div>
          <div>
            <p class="info-title">Address</p>
            <p class="info-detail">North Tower, Toronto, Canada</p>
          </div>
        </div>

        <div class="info-item">
          <div class="icon-box">💼</div>
          <div>
            <p class="info-title">Freelance</p>
            <p class="info-detail">Available Right Now</p>
          </div>
        </div>

        <div class="info-item">
          <div class="icon-box">✉️</div>
          <div>
            <p class="info-title">Email</p>
            <p class="info-detail">joe.miller@mydomain.com</p>
          </div>
        </div>

        <div class="info-item">
          <div class="icon-box">📞</div>
          <div>
            <p class="info-title">Phone</p>
            <p class="info-detail">+1 900 900 9000</p>
          </div>
        </div>
      </div>
    </div>

    <div class="right-side">
      <form class="contact-form">
        <input type="text" placeholder="YOUR FULL NAME *" />
        <input type="email" placeholder="YOUR EMAIL ADDRESS *" />
        <input type="text" placeholder="YOUR SUBJECT *" />
        <textarea placeholder="YOUR MESSAGE *"></textarea>
        <div class="terms">
          <input type="checkbox" id="terms" />
          <label for="terms">Accept the terms and conditions.</label>
        </div>
        <button type="submit">SEND MESSAGE</button>
      </form>
    </div>
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
  display: flex;
  width: 100%;
  min-height: 80vh; /* Mantendo a responsividade */
  color: #fff;
  padding: 20px 100px;
  align-items: center;

}

.posi-title{
  display: flex;
  flex-direction: column;

}

.left-side {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  flex: 1;
}

.right-side {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-title {
  font-size: 40px;
  letter-spacing: 2px;
  font-weight: bold;
}

.subtitle {
  font-size: 20px;
  margin-top: 10px;
  color: #aaa;
}

.subtitle span {
  color: #19e8ff;
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
  background-color: #2c2f34;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  margin-right: 15px;
  font-size: 20px;
}

.info-title {
  font-size: 16px;
  color: #aaa;
  margin-bottom: 5px;
}

.info-detail {
  font-size: 18px;
  color: #fff;
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
  border: 1px solid #555;
  padding: 15px 20px;
  margin-bottom: 20px;
  border-radius: 25px;
  color: #fff;
  font-size: 16px;
  outline: none;
}

.contact-form textarea {
  min-height: 150px;
  resize: none;
}

.terms {
  display: flex;
  align-items: center;
  color: #aaa;
  font-size: 14px;
  margin-bottom: 20px;
}

.terms input {
  margin-right: 10px;
}

.contact-form button {
  background: transparent;
  border: 1px solid #fff;
  color: #fff;
  padding: 15px;
  border-radius: 25px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s ease;
}

.contact-form button:hover {
  background-color: #fff;
  color: #1c1e22;
}
</style>
