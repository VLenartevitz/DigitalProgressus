<template>
    <section class="container">
        <div class="intro-wrapper">
            <p class="intro-text">
                Ao longo desses anos, já atendemos mais de 50 clientes, oferecendo desde o planejamento estratégico até
                a execução de campanhas de marketing digital, redes sociais e automação. Nosso trabalho se baseia na
                constante evolução das estratégias de marketing, acompanhando as tendências do mercado e utilizando as
                ferramentas mais modernas para garantir o sucesso de nossos parceiros.
            </p>
        </div>

        <div class="client-section">
            <img class="main-image" src="../assets/images/clube.png" alt="Imagem do cliente" />

            <div class="text-content">
                <h2 class="title">Cliente</h2>
                <p class="description">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt similique quibusdam expedita
                    magnam enim hic illum? Laudantium, deserunt?
                </p>
            </div>
        </div>

        <div class="image-gallery">
            <img class="image-small" src="../assets/images/clube.png" alt="Imagem pequena esquerda" />
            <img class="image-small" src="../assets/images/clube.png" alt="Imagem pequena direita" />
            <img class="image-medium" src="../assets/images/clube.png" alt="Imagem média" />
        </div>
    </section>
</template>

<script>
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';

gsap.registerPlugin(ScrollTrigger);

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Clients',
    mounted() {
        this.animateOnScroll();
    },
    methods: {
        animateOnScroll() {
            gsap.from('.intro-text', {
                opacity: 0,
                y: 50,
                duration: 1.5,
                ease: 'power4.out',
                scrollTrigger: {
                    trigger: '.intro-wrapper',
                    start: 'top 80%',
                    end: 'bottom 20%',
                    scrub: true,
                }
            });

            gsap.from('.main-image', {
                opacity: 0,
                scale: 0.8,
                duration: 1.5,
                ease: 'power4.out',
                scrollTrigger: {
                    trigger: '.client-section',
                    start: 'top 80%',
                    end: 'bottom 20%',
                    scrub: true,
                }
            });

            gsap.from('.client-section', {
                opacity: 0,
                x: -100,
                duration: 1.5,
                ease: 'power4.out',
                scrollTrigger: {
                    trigger: '.client-section',
                    start: 'top 80%',
                    end: 'bottom 20%',
                    scrub: true,
                }
            });

            gsap.from('.image-small, .image-medium', {
                opacity: 0,
                y: 50,
                stagger: 0.2,
                duration: 1,
                ease: 'power4.out',
                scrollTrigger: {
                    trigger: '.image-gallery',
                    start: 'top 80%',
                    end: 'bottom 20%',
                    scrub: true,
                }
            });
        }
    }
}
</script>

<style scoped>
.container {
    width: 90%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    color: #FAEFD1;
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
}

.main-image {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 15px;
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

.image-gallery {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    margin-top: 40px;
    width: 100%;
}

.image-small,
.image-medium {
    width: 100%;
    max-width: 350px;
    height: auto;
    border-radius: 10px;
}

/* Tablet (768px - 1024px) */
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
    
    .image-gallery {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
    }
    
    .image-small {
        width: calc(50% - 10px);
        max-width: 300px;
    }
    
    .image-medium {
        width: 100%;
        max-width: 500px;
    }
}

/* Desktop (1025px+) */
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
    
    .image-gallery {
        flex-direction: row;
        flex-wrap: nowrap;
    }
    
    .image-small {
        width: 30%;
    }
    
    .image-medium {
        width: 40%;
    }
}

/* Pequenos dispositivos móveis (até 480px) */
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
    
    .image-gallery {
        gap: 15px;
    }
}
</style>