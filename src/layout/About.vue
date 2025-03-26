<template>
    <div class="container">
        <p class="descriptionAbout">
            Somos uma <br/>Equipe formada<br/>por 4 irmãos ...
        </p>
        <div class="team">
            <div class="member">
                <img class="image" src="../assets/images/clube.png" />
                <p class="name">Daniel</p>
            </div>
            <div class="member">
                <img class="image" src="../assets/images/clube.png" />
                <p class="name">Samuel</p>
            </div>
            <div class="member">
                <img class="image" src="../assets/images/clube.png" />
                <p class="name">Filipe</p>
            </div>
            <div class="member">
                <img class="image" src="../assets/images/clube.png" />
                <p class="name">Gabriel</p>
            </div>
        </div>
        <div class="tamanhoTexto">
        <p class="footer-text">
            Desde 2019, atuamos com dedicação e comprometimento no mercado digital, ajudando empresas de diferentes segmentos a alcançar seu público-alvo e maximizar seu potencial de crescimento com nossos serviços.
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
      // Animação para a descrição da equipe
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

      // Animação para os membros da equipe
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
            delay: index * 0.2, // Delay entre animações dos membros
          }
        });
      });

      // Animação para o texto do rodapé
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
    align-items: flex-start;  /* Alinha o conteúdo à esquerda */
    justify-content: flex-start;  /* Ajusta para que o conteúdo comece do topo */
    width: 100%;
    background: #000;
    color: #fff;
    padding-left: 20px;  /* Adiciona um pequeno padding à esquerda */
}

.descriptionAbout {
    text-align: left;  /* Alinha o texto à esquerda */
    font-size: 80px;
    font-family: Montserrat;
    font-style: italic;
    font-weight: 900;
    color:rgba(250, 239, 209, 1);
    padding-left: 80px;
}

.team {
    display: flex;
    justify-content: center;  /* Centraliza as imagens */
    gap: 20px;
    width: 100%;  /* Garante que ocupe toda a largura disponível */
    margin-top: 40px;  /* Espaço entre a descrição e as imagens */
}

.member {
    text-align: center;
}

.image {
    width: 305px;
    height: 465px;
}

.name {
    font-size: 30px;
    font-family: Holtwood One SC;
    color: rgba(250, 239, 209, 1);
}

.footer-text {
    text-align: left;  /* Alinha o texto do rodapé à esquerda */
    font-size: 40px;
    font-family: Montserrat;
    font-weight: 400;
    padding: 40px;
    color: rgba(250, 239, 209, 1);
}

.tamanhoTexto{
    display: flex;
    padding: 40px 0px 0px 200px;
    width: 80%;
}


</style>
