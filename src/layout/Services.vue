<template>
  <div class="services-container">
    <div class="title">Serviços</div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>

    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao
            usuário.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Services",
};
</script>

<style scoped>
.services-container {
  display: flex;
  flex-direction: column;
  gap: 100px;
  /* Espaço entre as seções */
  padding-bottom: 200px;
  /* Garantir que o footer não sobreponha */
}

.service-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  text-align: center;
}

.service {
  display: flex;
}

.title {
  color: #faefd1;
  font-size: 80px;
  font-family: "Holtwood One SC";
  font-weight: 400;
  line-height: 80px;
}

.contentText {
  display: flex;
  flex-direction: column-reverse;
  justify-content: space-evenly;


}

.sub-title {
  color: #faefd1;
  font-size: 40px;
  font-family: "Montserrat";
  font-weight: 400;
  line-height: 40px;
  letter-spacing: 0.80px;
}

.description {
  color: white;
  font-size: 31px;
  font-family: "League Spartan";
  font-weight: 400;
  line-height: 31px;
  letter-spacing: 0.62px;
  word-wrap: break-word;
  margin: 20px 0;
}

.divider {
  width: 65px;
  border: 4px solid #faefd1;
}

.service-image {
  width: 100%;
  max-width: 703px;
  border-top-left-radius: 200px;
  border-top-right-radius: 200px;
}

@media (max-width: 768px) {
  .title {
    font-size: 60px;
  }

  .sub-title {
    font-size: 30px;
  }

  .description {
    font-size: 24px;
  }

  .service-image {
    max-width: 90%;
  }
}
</style>
