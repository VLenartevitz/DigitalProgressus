<template>
  <div class="container">
      <p class="descriptionAbout">
          Somos uma <br/>Equipe formada<br/>por 4 irmãos ...
      </p>
      <div class="team">
          <div class="member">
            <img class="image" src="../assets/images/filipe.png" />
            <p class="name">Daniel</p>
          </div>
          <div class="member">
              <img class="image" src="../assets/images/samuel.jpg" />
              <p class="name">Samuel</p>
          </div>
          <div class="member">
              <img class="image" src="../assets/images/filipe.png" />
              <p class="name">Filipe</p>
          </div>
          <div class="member">
              <img class="image" src="../assets/images/gab.png" />
              <p class="name">Gabriel</p>
          </div>
      </div>
      <div class="tamanhoTexto">
      <p class="footer-text">
          Desde 2020, atuamos com dedicação e comprometimento no mercado digital, ajudando empresas de diferentes segmentos a alcançar seu público-alvo e maximizar seu potencial de crescimento com nossos serviços.
      </p>
  </div>
  </div>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

gsap.registerPlugin(ScrollTrigger);

export default {
// eslint-disable-next-line vue/multi-word-component-names
name: "About",
mounted() {
  this.animateOnScroll();
},
methods: {
  animateOnScroll() {
    gsap.from('.descriptionAbout', {
      opacity: 0,
      y: -100,
      duration: 1.5,
      ease: 'power4.out',
      scrollTrigger: {
        trigger: '.descriptionAbout',
        start: 'top 80%',
        end: 'bottom 20%',
        scrub: true,
      }
    });

    const members = document.querySelectorAll('.member');

    members.forEach((member, index) => {
      gsap.from(member, {
        opacity: 0,
        y: 100,
        duration: 1.5,
        ease: 'power4.out',
        scrollTrigger: {
          trigger: member,
          start: 'top 80%',
          end: 'bottom 20%',
          scrub: true,
          delay: index * 0.2,
        }
      });
    });

    gsap.from('.footer-text', {
      opacity: 0,
      y: 100,
      duration: 1.5,
      ease: 'power4.out',
      scrollTrigger: {
        trigger: '.footer-text',
        start: 'top 80%',
        end: 'bottom 20%',
        scrub: true,
      }
    });
  }
}
}
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  background: #000;
  color: #fff;
  padding: 20px;
  box-sizing: border-box;
}

.descriptionAbout {
  text-align: center;
  font-size: 60px;
  /* font-family: Montserrat; */
  font-style: italic;
  font-weight: 900;
  color: rgba(250, 239, 209, 1);
  padding: 20px;
}

.team {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
  width: 100%;
  margin-top: 20px;
}

.member {
  text-align: center;
}

.image {
  width: 100%;
  max-width: 305px;
  height: auto;
}

.name {
  font-size: 24px;
  /* font-family: Holtwood One SC; */
  color: rgba(250, 239, 209, 1);
}

.footer-text {
  text-align: center;
  font-size: 24px;
  /* font-family: Montserrat; */
  font-weight: 400;
  padding: 20px;
  color: rgba(250, 239, 209, 1);
  width: 90%;
}

.tamanhoTexto {
  display: flex;
  justify-content: center;
  width: 100%;
}

/* Responsividade */
@media (max-width: 1200px) {
  .descriptionAbout {
      font-size: 50px;
  }
}

@media (max-width: 992px) {
  .descriptionAbout {
      font-size: 40px;
  }
  .name {
      font-size: 20px;
  }
}

@media (max-width: 768px) {
  .descriptionAbout {
      font-size: 30px;
  }
  .footer-text {
      font-size: 20px;
  }
}

@media (max-width: 576px) {
  .descriptionAbout {
      font-size: 24px;
  }
  .footer-text {
      font-size: 18px;
  }
  .name {
      font-size: 18px;
  }
}
</style>
