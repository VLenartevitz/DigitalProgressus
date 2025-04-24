<template>
  <div class="services-page">
    <h1 class="page-title">Nossos Serviços</h1>

    <div class="services-container">
      <div v-for="(service, index) in services" :key="index" class="service-card"
        :class="{ 'reverse-layout': index % 2 !== 0 }">
        <div class="service-content">
          <h3 class="service-title">{{ service.title }}</h3>
          <p class="service-description">{{ service.description }}</p>
          <button class="service-button" @click="scrollToContact">Saiba mais</button>
        </div>
        <div class="service-image-container">
          <img class="service-image" :src="getImageUrl(service.image)" :alt="service.title" />
          <div class="image-overlay"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

// Importe todas as imagens necessárias
import onlineWebDesign from '@/assets/images/online-web-design.jpg';
import videoProduction from '@/assets/images/influencer-showcasing-sound-mixer-device-viewers.jpg';
import design from '@/assets/images/design.jpg';
import ads from '@/assets/images/anuncios.png';
import socialMedia from '@/assets/images/midia.jpg';
import aiAssistant from '@/assets/images/ia.jpg';
import onlineCourses from '@/assets/images/desenvolvimento.png';

export default {
  name: "ServicesPage",
  data() {
    return {
      services: [
        {
          title: "Criação de Sites",
          description: "Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao usuário. Desde a criação do layout até a programação personalizada, garantimos que seu site seja não apenas visualmente atraente, mas também funcional e otimizado para SEO.",
          image: onlineWebDesign
        },
        {
          title: "Edição e Produção de Vídeo",
          description: "A produção de vídeos é uma das formas mais eficazes de conectar-se com seu público. Oferecemos serviços completos de edição e produção de vídeos, desde roteirização até a pós-produção, criando conteúdos que transmitem sua mensagem de forma clara e envolvente.",
          image: videoProduction
        },
        {
          title: "Design Gráfico",
          description: "A identidade visual é um dos pilares para o sucesso de qualquer marca. Nossa equipe de design cria materiais gráficos que traduzem a essência da sua marca de maneira única e impactante, garantindo que sua comunicação visual se destaque e seja reconhecida.",
          image: design
        },
        {
          title: "Gestão de Anúncios Online",
          description: "Aumente a conversão e maximize o retorno sobre o investimento com nossa gestão estratégica de anúncios online. Criamos campanhas otimizadas para alcançar o público certo e monitoramos os resultados em tempo real.",
          image: ads
        },
        {
          title: "Social Media",
          description: "Transforme sua presença digital com estratégias de Social Media personalizadas. Criamos conteúdos impactantes e desenvolvemos planos de engajamento para aumentar a visibilidade da sua marca nas redes sociais.",
          image: socialMedia
        },
        {
          title: "Atendente com IA",
          description: "Oferecemos soluções de atendimento ao cliente com Inteligência Artificial que proporcionam uma experiência de suporte ágil, eficiente e personalizada 24/7, liberando sua equipe para focar em questões estratégicas.",
          image: aiAssistant
        },
        {
          title: "Cursos Online",
          description: "Ajudamos você a lançar e monetizar cursos online com soluções completas de co-produção. Desde a criação do conteúdo até a plataforma de vendas, garantimos que seu curso seja atrativo e fácil de acessar.",
          image: onlineCourses
        }
      ]
    }
  },
  methods: {
    methods: {
      scrollToContact() {
        const contactSection = document.getElementById('contact');
        contactSection.scrollIntoView({ behavior: 'smooth' });
      }
    },
    getImageUrl(image) {
      return image;
    },
    setupAnimations() {
      gsap.registerPlugin(ScrollTrigger);

      // Animação do título
      gsap.from('.page-title', {
        opacity: 0,
        y: -50,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.page-title',
          start: 'top 80%',
          toggleActions: 'play none none none'
        }
      });

      // Animação dos cards de serviço
      gsap.utils.toArray('.service-card').forEach((card, index) => {
        gsap.from(card, {
          opacity: 0,
          y: 80,
          duration: 0.8,
          ease: 'back.out(1.2)',
          delay: index * 0.15,
          scrollTrigger: {
            trigger: card,
            start: 'top 75%',
            toggleActions: 'play none none none'
          }
        });
      });
    }
  },
  mounted() {
    this.setupAnimations();
  }
}
</script>

<style scoped>
.services-page {
  padding: 80px 20px;
  background: #000;
  color: #faefd1;
  min-height: 100vh;
}

.page-title {
  font-size: clamp(2.5rem, 6vw, 4.5rem);
  text-align: center;
  margin-bottom: 80px;
  background: linear-gradient(45deg, #faefd1, #ff9400);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  font-weight: 700;
  letter-spacing: 1px;
}

.services-container {
  display: flex;
  flex-direction: column;
  gap: 100px;
  max-width: 1400px;
  margin: 0 auto;
}

.service-card {
  display: flex;
  align-items: center;
  gap: 40px;
  position: relative;
}

.reverse-layout {
  flex-direction: row-reverse;
}

.service-content {
  flex: 1;
  padding: 40px;
  z-index: 2;
}

.service-title {
  font-size: clamp(1.8rem, 4vw, 2.5rem);
  color: #ff9400;
  margin-bottom: 20px;
  font-weight: 600;
}

.service-description {
  font-size: clamp(1rem, 1.8vw, 1.2rem);
  line-height: 1.6;
  color: rgba(250, 239, 209, 0.9);
  margin-bottom: 30px;
}

.service-button {
  background: linear-gradient(45deg, #ff9400, #ff6b00);
  color: #000;
  border: none;
  padding: 12px 30px;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(255, 148, 0, 0.3);
}

.service-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(255, 148, 0, 0.4);
}

.service-image-container {
  flex: 1;
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
  min-height: 400px;
}

.service-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, rgba(0, 0, 0, 0.7) 0%, transparent 100%);
}

.service-card:hover .service-image {
  transform: scale(1.05);
}

/* Responsividade */
@media (max-width: 1024px) {
  .services-container {
    gap: 70px;
  }

  .page-title {
    margin-bottom: 60px;
  }

  .service-card {
    flex-direction: column;
    gap: 30px;
  }

  .reverse-layout {
    flex-direction: column;
  }

  .service-content {
    padding: 30px;
    order: 2;
  }

  .service-image-container {
    width: 100%;
    min-height: 300px;
  }
}

@media (max-width: 768px) {
  .services-page {
    padding: 60px 15px;
  }

  .services-container {
    gap: 50px;
  }

  .page-title {
    margin-bottom: 40px;
  }

  .service-content {
    padding: 20px;
  }

  .service-title {
    margin-bottom: 15px;
  }

  .service-description {
    margin-bottom: 20px;
  }

  .service-button {
    padding: 10px 25px;
  }
}

@media (max-width: 480px) {
  .services-page {
    padding: 40px 10px;
  }

  .page-title {
    margin-bottom: 30px;
  }

  .service-card {
    gap: 20px;
  }

  .service-image-container {
    min-height: 250px;
  }
}
</style>