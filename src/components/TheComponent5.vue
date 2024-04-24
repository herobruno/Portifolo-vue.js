<template>
 <section id="sobre-component">
  <div class="container">
    <div class="content">
      <div class="texto">
        <h2 class="hero2">
          Sobre Mim
        </h2>
        <p class="descricao">
          Olá, meu nome é Bruno. Sou Full stack e atuo na área de desenvolvimento web. Sou aluno de Ciência da Computação na Universidade URI Santiago. Você pode me encontrar nas seguintes plataformas:<br>
        </p>
        <div class="contact-links">
      <a
        href="mailto:Brunoss2118@gmail.com"
        target="_blank"
      >
        <i class="far fa-envelope" />
        <span>Brunoss2118@gmail.com</span>
      </a>
      <a
        href="https://www.linkedin.com/in/bruno-souza-3b7682254/"
        target="_blank"
      >
        <i class="fab fa-linkedin" />
        <span>LinkedIn</span>
      </a>
      <a
        href="https://github.com/herobruno"
        target="_blank"
      >
        <i class="fab fa-github" />
        <span>GitHub</span>
      </a>
    </div>
      </div>
      <img class="imagem" src="../assets/AirBrush_20220920224806.jpg" alt="Imagem pequena">
    </div>
  </div>
</section>
<head>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.2/css/all.min.css"
    >
  </head>
</template>

<script>
export default {
  name: 'TheComponent5',
  data() {
    return {}
  },
}
</script>

<style scoped>

* {
  margin: 0;
  padding: 0;
}


html,
body {
  width: 100%;
  overflow-x: hidden;
}

#sobre-component {
  margin-top: 5%;
  background-color: #f4f4f4;
  padding: 1rem 0;
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 1s ease forwards;
  box-shadow: 0px 0px 5px 4px rgb(0, 0, 0);

}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
}

.content {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.imagem {
  max-width: 40%;
  border-radius: 50%;
  box-shadow: 0px 0px 5px 4px rgb(0, 0, 0);


}

.texto {
  max-width: 55%;
}

.hero2 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: #333;
}

.descricao {
  font-size: 1.2rem;
  color: #666;
  line-height: 1.6;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
h2 {
  color: #62ff00;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 10px;
  font-family:Arial, Helvetica, sans-serif;
}


@media (max-width: 768px) {
  #sobre-component {
   margin-top: 40%;
  }
  
  .container {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    padding: 40px;
  }
  
  .imagem {
    margin-right: 0;
    margin-bottom: 30px;
  }
}
h1{
  color:white;
  font-size: 20px;
}
.contact-icons {
    text-align: center;
    color: #efefef;
    margin-top: 20%;
  }

  .contact-links {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
  }

  .contact-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 20px 20px;
    font-size: 1.2rem;
    color: #0418f6;
    text-decoration: none;
    transition: color 0.2s ease-in-out;
  }

  .contact-links a:hover {
    color: #0077b5;
  }

  .contact-links i {
    margin-right: 10px;
    font-size: 1.5rem;
  }

  .contact-links span {
    margin-left: 5px;
  }


</style>