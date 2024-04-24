<template>

  <body>
    <header class="hero-header">
    <div class="hero">
      <h2 class="larger-text">{{ name }}</h2>
      <p class="typing-text larger-text">{{ typingText }}</p>
    </div>
  </header>
  </body>
  <section class="services">
    <h2> Meus Serviços</h2>
    <div class="service">
      <img src="../assets/Capa-post-1.png" alt="Serviço 1">
      <h3>Criação de WebSite</h3>
      <p>Crio sites personalizados para empresas,  ou projetos pessoais. Isso envolve a criação das páginas, estrutura, design e funcionalidades avançãdas..</p>
    </div>
    <div class="service">
      <img src="../assets/update.avif" alt="Serviço 2">
      <h3>Manutenção e Atualização</h3>
      <p>Forneço serviços de manutenção contínua para garantir que o site ou a aplicação esteja sempre funcionando corretamente e que as atualizações sejam implementadas de forma eficaz.</p>
    </div>
    <div class="service">
      <img src="../assets/robo.png" alt="Serviço 3">
      <h3>Desenvolvedor de Automação</h3>
      <p>Utilizo tecnologias e programação para criar sistemas que executam tarefas de forma automática, reduzindo a necessidade de intervenção humana repetitiva..</p>
    </div>
  </section>
 
</template>

<script>
export default {

  name: 'TheComponent1',
  data() {
    return {
      name: '',
      nameIndex: 0,
      textIndex: 0,
      typingText: ''
    }
  },
  mounted() {
    const typingInterval = setInterval(() => {
      if (this.textIndex >= this.introText.length) {
        clearInterval(typingInterval);
        return;
      }
      this.typingText += this.introText.charAt(this.textIndex);
      this.textIndex++;
    }, 100);

    const nameInterval = setInterval(() => {
      if (this.nameIndex >= this.nameText.length) {
        clearInterval(nameInterval);
        return;
      }
      this.nameIndex++;
      this.name = this.nameText.slice(0, this.nameIndex);
    }, 100);
  },
  computed: {
    nameText() {
      return 'Bruno Souza';
    },
    introText() {
      return 'Desenvolvedor Web';
    }
  }
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
}

html, body {

  overflow-x: hidden;
}

.larger-text {
  font-size: 30px; 
  font-family:Arial, Helvetica, sans-serif;
  
}
.services {
  color: #fff;
  padding: 1rem 0;
  text-align: center;
  overflow: hidden; 
  margin-bottom: 5%;
  box-shadow: 0px 0px 5px 4px rgb(0, 0, 0);
  border-radius: 1%;
  margin-top: 5%;
 
}

.services h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #00f01c;
  font-family:Arial, Helvetica, sans-serif;
  
}

.service {
  width: 30%;
  height: 30%;
  display: inline-block;
  margin: 1rem;
  padding: 1.5rem;
  border-radius: 10px;
  background-color: #000000; 
}

.service img{
  width: 500px;
  height:300px;
}


.service h3 {
  font-size: 1.5rem;
  margin: 1rem 0;
  color: #00f01c;
  font-family:Arial, Helvetica, sans-serif;
  
}

.service p {
  font-size: 1rem;
  font-family:Arial, Helvetica, sans-serif;
}


body {
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-header {
  position: sticky;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1;
  margin-top: 10%;
 
}

.hero {
  position: relative;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #37ff00;
  overflow: hidden;
  width: 100%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
 
}

.typing-text {
  display: inline-block;
  border-right: 0.15em solid orange;
  animation: typing 3s steps(40, end) forwards, blink-text 0.5s step-end infinite;
  white-space: nowrap;
  overflow: hidden;
  width: 0;
  font-weight: bold;
  font-family:Arial, Helvetica, sans-serif;
}
.typing-text::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0.15em;
  height: 1.1em;
  background-color: orange;
  animation: cursor 2s steps(40, end) infinite;
  font-family:Arial, Helvetica, sans-serif;
}


@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}

@keyframes blink-text {
  from {
    border-right-color: orange;
  }
  to {
    border-right-color: transparent;
  }
}

@keyframes cursor {
  from, to {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}


@media screen and (min-width: 320px) and (max-width: 575px) {
  .services {
    text-align: center;
  }

  .service {
    width: 90%; 
    margin: 1rem auto;
  }

  .service img {
    max-width: 100%; 
    height: auto;
  }
}

/* Media query para telas médias (a partir de 576px até 991px) */
@media screen and (min-width: 576px) and (max-width: 991px) {
  .services {
    text-align: center;
  }

  .service {
    width: 45%; 
    margin: 1rem;
  }

  .service img {
    max-width: 100%; 
    height: auto;
  }
}

/* Media query para telas maiores (a partir de 992px até 1800px) */
@media screen and (min-width: 992px) and (max-width: 1800px) {
 
  .service img {
    max-width: 100%; 
    height: auto;
  }
}


</style>