<template>
    <div id="tectudo">
        <h1>Tecnologias</h1>
    </div>
    <section class="tecnologias">
     
     
      <div class="logo">
        <div class="logo-container">
          <img src="https://cdn.iconscout.com/icon/free/png-512/javascript-2752148-2284965.png">
          <span class="classe-do-elemento">JavaScript</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://nodejs.org/static/images/logo.svg">
          <span class="classe-do-elemento">Node.Js</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://expressjs.com/images/express-facebook-share.png">
          <span class="classe-do-elemento">Express.js</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://getbootstrap.com/docs/5.1/assets/brand/bootstrap-logo-shadow.png">
          <span class="classe-do-elemento">BootsTrap</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://cdn.iconscout.com/icon/free/png-256/html5-40-1175193.png">
          <span class="classe-do-elemento">HTML</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://cdn.iconscout.com/icon/free/png-512/css3-11-1175239.png">
          <span class="classe-do-elemento">CSS3</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://vuejs.org/images/logo.png">
          <span class="classe-do-elemento">Vue.Js</span>
        </div>
      </div>
      <div class="logo">
        <div class="logo-container">
          <img src="https://cdn.iconscout.com/icon/free/png-512/mysql-19-1174939.png">
          <span class="classe-do-elemento">Mysql</span>
        </div>
      </div>
      <div class="logo">
    <div class="logo-container">
      <img src="../assets/0_xZfzHRVLm4z4NE5Z.png">
      <span class="classe-do-elemento">SQL</span>
    </div>
  </div>
  <div class="logo">
    <div class="logo-container">
      <img src="../assets/c-logo.png">
      <span class="classe-do-elemento">C</span>
    </div>
  </div>
  <div class="logo">
    <div class="logo-container">
      <img src="../assets/68747470733a2f2f692e696d6775722e636f6d2f79764559686e5a2e706e67.png">
      <span class="classe-do-elemento">Sequelize</span>
    </div>
  </div>
  <div class="logo">
    <div class="logo-container">
      <img src="../assets/Typescript.svg.png">
      <span class="classe-do-elemento">TypeScript</span>
    </div>
  </div>
    </section>
   
  
  </template>
  
  <script>
  export default {
    name: 'TheComponent4',
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
 
.tecnologias {
  font-family:Arial, Helvetica, sans-serif;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 1rem;
 
}

.logo {
  flex: 0 0 calc(25% - 2rem);
  margin: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-radius: 5rem;
  box-shadow: 0px 0px 5px 4px rgba(255, 255, 255, 0.2);
  padding: 1rem;
  box-sizing: border-box;
  transition: transform 0.3s, box-shadow 0.3s;
  background-color: black;
}

.logo:hover {
  transform: scale(1.05);
  box-shadow: 10px 10px 20px rgba(255, 255, 255, 0.3);
}

.logo img {
  width: 70px;
  height: auto;
}

.classe-do-elemento {
  font-weight: bold;
  text-align: left;
  color: rgb(0, 255, 17);
  font-size: 20px;
  padding: 5px;
  border-radius: 10%;
  margin-left: 1rem;
}

.logo-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}


h1 {
  color: #fff;
  font-size: 20px;
  text-align: center;
  justify-content: center;
  align-items: center;

}
.comment {
  background-color: #1c1616;
  border-left: 4px solid #62ff00;
  padding: 1rem;
  margin: 1rem;
  max-width: 70%;
  position: relative;
  margin-top: 5%;
}

.quote-icon {
  font-size: 24px;
  color: #62ff00;
  position: absolute;
  top: -20px;
  left: -20px;
}

.quote-text {
  font-size: 18px;
  text-align: left;
  margin-bottom: 0.5rem;
  color: #ffffff;
}

.author {
  font-size: 14px;
  font-style: italic;
  color: #ffffff;
  text-align: right;
}
@media (max-width: 768px) {
  .tecnologias {
    justify-content: center; 
  }

  .logo {
    flex: 0 0 calc(100% - 2rem); 
    margin: 1rem 0;
  }

  .logo img {
    width: 60px;
    height: 60px;
  }

  .classe-do-elemento {
  /* ... outros estilos ... */
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
  .logo-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 120%;
    height: 100%;
    background-color: black;
    border-radius: 5rem;
    box-shadow: 0px 0px 5px 4px rgba(255, 255, 255, 0.2);
    transition: transform 0.3s, box-shadow 0.3s;
  }
  .comment {
    margin-bottom: 20%;
  }

  .logo:hover {
    transform: scale(1.05);
    box-shadow: 10px 10px 20px rgba(255, 255, 255, 0.3);
  }
}
#tectudo{
  width: 100%;
  display: flex;
  justify-content: center;
  font-family:Arial, Helvetica, sans-serif;
  margin-top: 15%;
  
}
#tectudo h1{
  color: #62ff00;
  font-size: 24px;
}
@media screen and (min-width: 769px) and (max-width: 1096px) {
  .tecnologias {
    justify-content: space-between; 
  }

  .logo {
    flex: 0 0 calc(33.33% - 2rem); 
    margin: 1rem;
  }

  .logo img {
    width: 70px; 
    height: auto; 
  }

  .classe-do-elemento {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column; 
  }

  .logo-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
    background-color: black;
    border-radius: 5rem;
    box-shadow: 0px 0px 5px 4px rgba(255, 255, 255, 0.2);
    transition: transform 0.3s, box-shadow 0.3s;
  }

  .comment {
    margin-bottom: 10%;
  }

  .logo:hover {
    transform: scale(1.05);
    box-shadow: 10px 10px 20px rgba(255, 255, 255, 0.3);
  }
}


   </style>