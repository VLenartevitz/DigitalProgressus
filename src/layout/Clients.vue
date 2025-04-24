<template>
  <section class="container">
    <div class="intro-wrapper">
      <p class="intro-text">
        Ao longo desses anos, já atendemos mais de 60 clientes em todo Brasil,
        oferecendo desde o planejamento estratégico até a execução de campanhas
        de marketing digital, redes sociais e automação. Nosso trabalho se
        baseia na constante evolução das estratégias de marketing, acompanhando
        as tendências do mercado e utilizando as ferramentas mais modernas para
        garantir o sucesso de nossos parceiros.
      </p>
    </div>

    <!-- Seção de Depoimentos -->
    <div class="client-section">
      <img
        class="main-image"
        :src="testimonials[currentTestimonialIndex].image"
        :alt="`Depoimento ${testimonials[currentTestimonialIndex].title}`"
      />

      <div class="text-content">
        <h2 class="title">{{ testimonials[currentTestimonialIndex].title }}</h2>
        <p class="description">{{ testimonials[currentTestimonialIndex].description }}</p>
      </div>
    </div>

    <!-- Carrossel de Logos -->
    <div class="logo-carousel">
      <h3 class="carousel-title">Alguns de nossos clientes</h3>
      <div class="carousel-track">
        <div class="carousel-slide" v-for="(logo, index) in [...logos, ...logos]" :key="index">
          <img 
            class="logo-image" 
            :src="logo.image" 
            :alt="`Logo ${logo.name}`"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { gsap } from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";

// Imagens para depoimentos (fotos reais)
import logoMav from "@/assets/images/Logo MAV.jpg";
import logoCatelao from "@/assets/images/Logo Catelão.jpg";
import logoOneHep from "@/assets/images/Logo One Hep.jpg";
import kauamImage from "@/assets/images/Kauam.jpg";
import valterImage from "@/assets/images/Valter.jpg";
import ClubeImage from "@/assets/images/clube.png";
import OssImage from "@/assets/images/oss.png";



gsap.registerPlugin(ScrollTrigger);

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Clients",
  data() {
    return {
      // Array para depoimentos (com fotos dos clientes)
      testimonials: [
        {
          title: "MAV",
          description:
            "Realizam serviços de maneira correta e super prestativos. Trazem resultados significativos e soluções para qualquer situação.  MAV Company - Agência de Publicidade",
          image: logoMav,
        },
        {
          title: "Catelão",
          description:
            "Gostei muito do trabalho da Prógressus, as campanhas conseguiram performar muito bem sem um custo muito alto, fora que conseguimos atingir todos os objetivos de campanhas. Top demais! Catelão Distribuidora - Distribuidora de Peças Automotivas",
          image: logoCatelao,
        },
        {
          title: "One Hep",
          description:
            "Gostaria de agradecer os serviços da Prógressus. Geraram bastante resultado pra gente, valeu pela atenção. One Help - Manutenção Informática",
          image: logoOneHep,
        },
        {
          title: "Kauam",
          description:
            "A Prógressus é um exemplo em dedicação e resultados. Sempre preocupados com os resultados e trazendo estratégias únicas para cada negócio e projeto. Kauam Pagliarini - Infoprodutor",
          image: kauamImage,
        },
        {
          title: "Valter",
          description:
            "Atenciosos, aplicados e entregam um serviço de qualidade. Já passei por 4 agências e a Prógressus foi a única que trouxe resultados sólidos. Valter Serafim - Infoprodutor",
          image: valterImage,
        },
      ],
      
      logos: [
        { name: "MAV Company", image: logoMav },
        { name: "Catelão Distribuidora", image: logoCatelao },
        { name: "One Hep", image: logoOneHep },
        { name: "Kauam", image: kauamImage },
        { name: "Valter", image: valterImage },
        { name: "Fibradoss", image: OssImage },
        { name: "Costela", image: ClubeImage },

      ],
      
      currentTestimonialIndex: 0,
      intervalId: null
    };
  },
  mounted() {
    this.animateOnScroll();
    this.startTestimonialRotation();
    this.setupLogoCarousel();
  },
  beforeUnmount() {
    clearInterval(this.intervalId);
  },
  methods: {
    animateOnScroll() {
      gsap.from(".intro-text", {
        opacity: 0,
        y: 50,
        duration: 1.5,
        ease: "power4.out",
        scrollTrigger: {
          trigger: ".intro-wrapper",
          start: "top 80%",
          end: "bottom 20%",
          scrub: true,
        },
      });

      gsap.from(".main-image", {
        opacity: 0,
        scale: 0.8,
        duration: 1.5,
        ease: "power4.out",
        scrollTrigger: {
          trigger: ".client-section",
          start: "top 80%",
          end: "bottom 20%",
          scrub: true,
        },
      });

      gsap.from(".client-section", {
        opacity: 0,
        x: -100,
        duration: 1.5,
        ease: "power4.out",
        scrollTrigger: {
          trigger: ".client-section",
          start: "top 80%",
          end: "bottom 20%",
          scrub: true,
        },
      });

      gsap.from(".logo-carousel", {
        opacity: 0,
        y: 50,
        duration: 1,
        ease: "power4.out",
        scrollTrigger: {
          trigger: ".logo-carousel",
          start: "top 80%",
          end: "bottom 20%",
          scrub: true,
        },
      });
    },
    
    startTestimonialRotation() {
      this.intervalId = setInterval(() => {
        this.currentTestimonialIndex = 
          (this.currentTestimonialIndex + 1) % this.testimonials.length;
      }, 6000);
    },
    
    setupLogoCarousel() {
      this.$nextTick(() => {
        const track = document.querySelector('.carousel-track');
        if (!track) return;
        
        const width = track.scrollWidth / 2;
        
        gsap.to(track, {
          x: -width,
          duration: 40,
          ease: "none",
          repeat: -1
        });
      });
    }
  }
};
</script>

<style scoped>
.container {
  width: 90%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  color: #faefd1;
  padding: 20px 0;
}

.intro-wrapper {
  width: 100%;
  margin-bottom: 40px;
}

.intro-text {
  font-size: 28px;
  line-height: 1.4;
}

.client-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 30px;
  text-align: center;
  width: 100%;
  margin: 40px 0;
}

.main-image {
  width: 100%;
  max-width: 500px;
  height: auto;
  border-radius: 15px;
  object-fit: cover;
  aspect-ratio: 1/1;
}

.text-content {
  width: 100%;
}

.title {
  font-size: 36px;
  line-height: 1.2;
  margin-bottom: 15px;
}

.description {
  font-size: 20px;
  line-height: 1.5;
}

/* Estilos do Carrossel de Logos */
.logo-carousel {
  width: 100%;
  overflow: hidden;
  margin: 80px 0;
  padding: 40px 0; /* Aumentei o padding */
  position: relative;
  background: rgba(255, 255, 255, 0.05); /* Fundo sutil para destacar */
  border-radius: 15px;
}

.carousel-track {
  display: flex;
  gap: 60px; /* Aumentei o espaçamento */
  width: max-content;
  will-change: transform;
  align-items: center; /* Centraliza verticalmente */
  padding: 20px 0;
}

.logo-image {
  height: 120px; /* Aumentei significativamente o tamanho */
  width: auto;
  max-width: 220px;
  object-fit: contain;
  opacity: 0.9; /* Removi o grayscale e ajustei a opacidade */
  transition: all 0.3s ease;
}

.logo-image:hover {
  opacity: 1;
  transform: scale(1.15); /* Efeito hover mais pronunciado */
}

/* Responsividade */
@media (min-width: 768px) {
  .intro-text {
    font-size: 32px;
  }

  .client-section {
    flex-direction: row;
    justify-content: center;
    text-align: left;
  }

  .main-image {
    width: 50%;
  }

  .text-content {
    width: 45%;
  }

  .title {
    font-size: 42px;
  }

  .description {
    font-size: 24px;
  }

  .logo-image {
    height: 150px;
    max-width: 250px;
  }
}

@media (min-width: 1025px) {
  .container {
    width: 80%;
  }

  .intro-text {
    font-size: 36px;
  }

  .title {
    font-size: 48px;
  }

  .description {
    font-size: 28px;
  }

  .carousel-title {
    font-size: 32px;
  }

  .logo-image {
    height: 180px;
    max-width: 300px;
  }
  
  .carousel-track {
    gap: 80px;
  }
}

@media (max-width: 480px) {
  .intro-text {
    font-size: 22px;
  }

  .title {
    font-size: 30px;
  }

  .description {
    font-size: 18px;
  }

  .logo-image {
    height: 80px;
    max-width: 150px;
  }
  
  .carousel-track {
    gap: 30px;
  }
}
</style>