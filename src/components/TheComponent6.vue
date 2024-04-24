<template>
  <div class="project-container">
    <h1 style="text-align: left;">Projetos</h1>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div v-for="(project, index) in projects" :key="index" class="swiper-slide project-card">
          <div class="project-image">
            <img :src="require(`@/assets/${project.image}`)" :alt="project.title">
          </div>
          <div class="project-details">
            <h2>{{ project.title }}</h2>
            <p>{{ project.description }}</p>
            <div class="buttons">
              <a :href="project.liveLink" class="button">View Live</a>
              <a :href="project.gitRepoLink" class="button">Git Repo</a>
            </div>
          </div>
        </div>
      </div>
      <div class="swiper-button-prev"></div>
      <div class="swiper-button-next"></div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';

export default {
  data() {
    return {
      projects: [
        {
          title: 'Classic Car',
          description: 'Software de venda de carros totalmente intuitivo e documentado ',
          image: 'classic.jpg',
          liveLink: '',
          gitRepoLink: 'https://github.com/herobruno/clasicar',
        },
        {
          title: 'Despesas auto',
          description: 'Algoritmo para automatizar despesas de casa criado com a linguagem portugal',
          image: 'pagamento.jpg',
          liveLink: '',
          gitRepoLink: 'https://github.com/herobruno/Automatizador-de-despesas',
        },
        {
          title: 'Portfólio',
          description: 'Portfólio WEB criado utilizando a tecnologia Vue js e java script ',
          image: 'portifolio.png',
          liveLink: 'https://example.com/projeto3',
          gitRepoLink: 'https://github.com/user/projeto3',
        },
        // Adicione mais projetos conforme necessário
      ],
      swiper: null,
    };
  },
  mounted() {
    this.swiper = new Swiper('.swiper-container', {
      slidesPerView: 2, // Exibir 2 projetos inicialmente
      spaceBetween: 20,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    });
  },
};
</script>

<style scoped>
html, body {
  overflow-x: hidden;
}
.swiper-button-prev,


.swiper-button-next{
  display: none;

  
}
 
.project-container {
  text-align: left;
  padding: 5px;
  max-width: 50%; 
  margin: 0 auto; 
  overflow-x: hidden; 
}


h1 {
  font-size: 24px;
  text-align: left;
  margin-bottom: 20px;
  color: rgb(0, 255, 17);
  margin-top: 10%;
  font-family:Arial, Helvetica, sans-serif;
  
}

.swiper-container {
  display: flex;
  justify-content: space-between;
}

.project-card {
  width: 10%; 
  border-radius: 5px;
  padding: 20px;
  margin-bottom: 20px;
  box-shadow: 0px 0px 5px 4px rgb(0, 0, 0);
}

.project-image {
  margin-bottom: 10px;
}

.project-image img {
  max-width: 100%;
  max-height: 100%;
  border-radius: 2%;
  box-shadow: 0px 0px 10px  rgb(38, 255, 0);
}

.project-details {
  text-align: center;
  color: #fff;
}

h2 {
  font-size: 18px;
  margin-bottom: 10px;
  font-family:Arial, Helvetica, sans-serif;
  color: #00ff00;
}

.buttons {
  display: flex;
  justify-content: center;
  margin-top: 10px;

}

.button {
  display: inline-block;
  margin: 0 5px;
  padding: 10px 20px;
  background-color: #000000;
  color: #fff;
  text-decoration: none;
  border-radius: 5px;
  cursor: pointer;
  font-family:Arial, Helvetica, sans-serif;
}

.button:hover {
  background-color: #0056b3;
}
@media (max-width: 768px) {
  .project-container {
    max-width: 90%; 

  }
  
  .project-card {
    width: 45%; 
  }
}

/* Media query para telas menores que 576px */
@media (max-width: 576px) {
  .project-container {
    max-width: 100%; 
  
  }
  
  .project-card {
    width: 100%;
  }
  
  
  
  
}
</style>
