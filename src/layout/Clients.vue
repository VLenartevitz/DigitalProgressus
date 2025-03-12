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
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Clients'
}
</script>

<style scoped>
.container {
    width: 80%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    color: #FAEFD1;
    font-family: 'Gentium Book Plus', serif;
}

.intro-wrapper {
    width: 90%;
    margin-bottom: 20px;
}

.intro-text {
    font-size: 50px;
}

.client-section {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    text-align: left;
}

.main-image {
    width: 50%;
    max-width: 539px;
    height: auto;
}

.title {
    font-size: 70px;
    line-height: 70px;
    margin-bottom: 10px;
}

.description {
    font-size: 50px;
}

.image-gallery {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    margin-top: 30px;
}

.image-small,
.image-medium {
    width: 100%;
    max-width: 300px;
    height: auto;
}
</style>
