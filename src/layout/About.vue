<template>
    <div class="container">
        <p class="description">
            Somos uma <br/>Equipe formada<br/>por 4 irmãos ...
        </p>
        <div class="team">
            <div class="member">
                <img class="image" src="https://via.placeholder.com/205x365" />
                <p class="name">Daniel</p>
            </div>
            <div class="member">
                <img class="image" src="https://via.placeholder.com/205x364" />
                <p class="name">Samuel</p>
            </div>
            <div class="member">
                <img class="image" src="https://via.placeholder.com/205x364" />
                <p class="name">Filipe</p>
            </div>
            <div class="member">
                <img class="image" src="https://via.placeholder.com/205x364" />
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
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "About",
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

.description {
    text-align: left;  /* Alinha o texto à esquerda */
    font-size: 80px;
    font-family: Montserrat;
    font-style: italic;
    font-weight: 900;
    color: #fff;
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
    color: #fff;
}

.footer-text {
    text-align: left;  /* Alinha o texto do rodapé à esquerda */
    font-size: 40px;
    font-family: Montserrat;
    font-weight: 400;
    padding: 40px;
}

.tamanhoTexto{
    display: flex;
    padding: 40px 0px 0px 200px;
    width: 80%;
}


</style>
