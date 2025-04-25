<template >
<section id="sobre-nos">
  <div class="about-container">
    <div class="hero-section">
      <p class="descriptionAbout">
        Somos uma <br/>Equipe formada<br/>por 4 irmãos
      </p>
    </div>

    <div class="team-section">
      <div class="team">
        <div class="member" v-for="(member, index) in teamMembers" :key="index">
          <div class="image-wrapper">
            <img class="member-image" :src="member.image" :alt="`Foto de ${member.name}`" />
            <div class="overlay"></div>
          </div>
          <p class="name">{{ member.name }}</p>
        </div>
      </div>
    </div>

    <div class="footer-section">
      <p class="footer-text">
        Desde 2020, atuamos com dedicação e comprometimento no mercado digital, 
        ajudando empresas de diferentes segmentos a alcançar seu público-alvo e 
        maximizar seu potencial de crescimento com nossos serviços.
      </p>
    </div>
  </div>
</section>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

// Importe as imagens corretas para cada membro
import danielImage from '@/assets/images/dani.png';
import samuelImage from '@/assets/images/samuel.jpg';
import filipeImage from '@/assets/images/filipe.png';
import gabrielImage from '@/assets/images/gab.png';

gsap.registerPlugin(ScrollTrigger);

export default {
  name: "AboutPage",
  data() {
    return {
      teamMembers: [
        { name: "Daniel", image: danielImage,  },
        { name: "Samuel", image: samuelImage,  },
        { name: "Filipe", image: filipeImage,  },
        { name: "Gabriel", image: gabrielImage,  }
      ]
    };
  },
  mounted() {
    this.animateOnScroll();
  },
  methods: {
    animateOnScroll() {
      // Animação do título
      gsap.from('.descriptionAbout', {
        opacity: 0,
        y: -50,
        duration: 1.2,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.hero-section',
          start: 'top 75%',
          toggleActions: 'play none none none'
        }
      });

      // Animação dos membros da equipe
      gsap.utils.toArray('.member').forEach((member, index) => {
        gsap.from(member, {
          opacity: 0,
          y: 50,
          duration: 0.8,
          ease: 'back.out(1.2)',
          delay: index * 0.15,
          scrollTrigger: {
            trigger: '.team-section',
            start: 'top 70%',
            toggleActions: 'play none none none'
          }
        });
      });

      // Animação do texto do rodapé
      gsap.from('.footer-text', {
        opacity: 0,
        y: 30,
        duration: 1,
        ease: 'power2.out',
        scrollTrigger: {
          trigger: '.footer-section',
          start: 'top 80%',
          toggleActions: 'play none none none'
        }
      });
    }
  }
}
</script>

<style scoped>
.about-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  background: #000;
  color: #faefd1;
  overflow: hidden;
}

.hero-section {
  width: 100%;
  padding: 80px 20px;
  text-align: center;
  background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7));
}

.descriptionAbout {
  font-size: clamp(2.5rem, 8vw, 5rem);
  font-style: italic;
  font-weight: 900;
  line-height: 1.2;
  margin: 0;
  background: linear-gradient(45deg, #faefd1, #c8b48c);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.team-section {
  width: 100%;
  padding: 60px 20px;
  background: #000;
}

.team {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  max-width: 1400px;
  margin: 0 auto;
}

.member {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.image-wrapper {
  position: relative;
  width: 100%;
  max-width: 280px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(250, 239, 209, 0.1);
  margin-bottom: 20px;
  transition: transform 0.3s ease;
}

.image-wrapper:hover {
  transform: translateY(-10px);
}

.member-image {
  width: 100%;
  height: 350px;
  object-fit: cover;
  display: block;
  transition: transform 0.5s ease;
}

.image-wrapper:hover .member-image {
  transform: scale(1.05);
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.7) 0%, transparent 40%);
}

.name {
  font-size: 1.8rem;
  font-weight: 700;
  margin: 10px 0 5px;
  color: #faefd1;
}

.role {
  font-size: 1.1rem;
  color: rgba(250, 239, 209, 0.8);
  margin: 0;
}

.footer-section {
  width: 100%;
  padding: 80px 20px;
  background: #111;
  text-align: center;
}

.footer-text {
  font-size: clamp(1.1rem, 3vw, 1.4rem);
  line-height: 1.6;
  max-width: 900px;
  margin: 0 auto;
  color: rgba(250, 239, 209, 0.9);
}

/* Responsividade */
@media (max-width: 768px) {
  .hero-section {
    padding: 60px 20px;
  }
  
  .team {
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
  }
  
  .member-image {
    height: 300px;
  }
}

@media (max-width: 480px) {
  .team {
    grid-template-columns: 1fr;
  }
  
  .hero-section {
    padding: 40px 20px;
  }
  
  .footer-section {
    padding: 60px 20px;
  }
}
</style>