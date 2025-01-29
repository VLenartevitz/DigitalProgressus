<template>
  <div class="services-container">
    <div class="title">Serviços</div>

    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Desenvolvemos sites responsivos, rápidos e com design intuitivo que oferecem uma excelente experiência ao usuário. Desde a criação do layout até a programação personalizada, garantimos que seu site seja não apenas visualmente atraente, mas também funcional e otimizado para SEO. Com nossa expertise, seu negócio estará online com uma plataforma que reflete sua identidade e potencializa sua presença digital.
          </div>
          <div class="sub-title">Criação de Sites</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service2">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            A produção de vídeos é uma das formas mais eficazes de conectar-se com seu público. Oferecemos serviços completos de edição e produção de vídeos, desde roteirização até a pós-produção, criando conteúdos que transmitem sua mensagem de forma clara e envolvente. Seja para vídeos institucionais, campanhas publicitárias ou conteúdos para redes sociais, nossa equipe transforma sua visão em realidade.
          </div>
          <div class="sub-title">Edição e Produção de Vídeo</div>
        </div>
        <img class="service-image2" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            A identidade visual é um dos pilares para o sucesso de qualquer marca. Nossa equipe de design cria materiais gráficos que traduzem a essência da sua marca de maneira única e impactante. Desenvolvemos logotipos, material promocional, banners, infográficos e muito mais, com foco em estética e funcionalidade, garantindo que sua comunicação visual se destaque e seja reconhecid
          </div>
          <div class="sub-title">DESIGN</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service2">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Aumente a conversão e maximize o retorno sobre o investimento (ROI) com nossa gestão estratégica de anúncios online. Criamos campanhas de publicidade paga no Google Ads, Facebook, Instagram e outras plataformas, otimizando cada anúncio para alcançar o público certo. Monitoramos os resultados em tempo real e ajustamos as campanhas conforme necessário para garantir o melhor desempenho.
          </div>
          <div class="sub-title">Gestão de Anúncios Online</div>
        </div>
        <img class="service-image2" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Transforme sua presença digital com estratégias de Social Mídia personalizadas. Nossa equipe cria conteúdos impactantes e desenvolve planos de engajamento para aumentar a visibilidade da sua marca nas redes sociais. Utilizamos as melhores práticas para promover uma comunicação consistente e eficaz, gerando conexões reais com seu público e conquistando resultados de longo prazo.
          </div>
          <div class="sub-title">Social Mídia</div>
        </div>
        <img class="service-image" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service2">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Oferecemos soluções de atendimento ao cliente com Inteligência Artificial (IA), que proporcionam uma experiência de suporte ágil, eficiente e personalizada. Nossos sistemas de IA podem responder dúvidas frequentes, processar solicitações e até mesmo realizar vendas, tudo de forma automatizada, 24/7, liberando sua equipe para focar em questões mais complexas e estratégicas
          </div>
          <div class="sub-title">Atendente com Inteligência Artificial </div>
        </div>
        <img class="service-image2" :src="require('@/assets/images/Logo.png')" alt="Criação de Sites" />
      </div>
    </div>
    <div class="service-section">
      <div class="service">
        <!-- <div class="divider"></div> -->
        <div class="contentText">
          <div class="description">
            Ajudamos você a lançar e monetizar cursos online com soluções completas de co-produção. Desde a criação do conteúdo até a plataforma de vendas, garantimos que seu curso seja atrativo e fácil de acessar para seus alunos. Trabalhamos juntos para maximizar o alcance e as vendas, utilizando estratégias de marketing digital para promover seu curso e atrair um público engajado e qualificado.
          </div>
          <div class="sub-title">Co-Produção para Venda de Cursos Online</div>
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
  padding-bottom: 200px;
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
  padding-left: 20px;
}
.service2 {
  display: flex;
  flex-direction: row-reverse;
  padding-right: 20px;

}

.title {
  color: #faefd1;
  font-size: 80px;
  font-family: "Holtwood One SC";
  font-weight: 400;
  line-height: 80px;
  padding-left: 100px;
}

.contentText {
  display: flex;
  flex-direction: column-reverse;
  justify-content: space-evenly;
  width: 100%;
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
  font-weight: 300;
  line-height: 31px;
  letter-spacing: 0.62px;
  margin: 20px ;
}

.divider {
  width: 65px;
  border: 4px solid #faefd1;
}

.service-image {
  width: 100%;
  max-width: 703px;
  border-top-left-radius: 200px;
  border-bottom-left-radius: 200px;
}

.service-image2 {
  width: 100%;
  max-width: 703px;
  border-top-right-radius: 200px;
  border-bottom-right-radius: 200px;
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
