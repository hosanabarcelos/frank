<template>
  <div class="home__container">
        <div class="home__container-content">
            <div class="home__content">
                <lottie
                    :options="defaultOptions"
                    :width="90"
                    :height="90"
                />
                <h2>{{ title }}</h2>
                <p>{{ subtitle }}</p>
                <primary-button
                    path="/chat"
                    text="Iniciar atendimento"
                />
            </div>
        </div>
  </div>
</template>

<script>
import * as animationData from '../assets/animations/robot.json';
import PrimaryButton from '../components/PrimaryButton.vue';

export default {
    name: 'Home',
    data() {
        return {
            title: 'Olá, querido(a) cliente!',
            subtitle: 'Eu sou o Frank e vou dar início ao seu atendimento. Preciso que você responda algumas perguntas para conseguirmos agilizar o seu pedido. Vamos lá?',
            defaultOptions: {
                animationData: animationData
            }
        }
    },
    components: {
        PrimaryButton,
    }
}
</script>

<style scoped>

.home__container {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #424783;
}
.home__container-content {
    height: 400px;
    width: 350px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-radius: 1rem;
    background-color: #FAF7FD;
    z-index: 5;
}
.home__content {
    margin: 2.5rem;
    text-align: center;
}
h2 {
    font-size: 16px;
    font-weight: 500;
}
p {
    font-size: 12px;
    font-weight: 400;
    line-height: 18px;
}
a {
    text-decoration: none;
}
</style>
