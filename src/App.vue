<template>
 <div>
    <nav>
      <div class="navbar-header">
        <button class="menu-toggle" @click="toggleMenu" v-if="shouldShowIcon">
          <img class="menu-icon" src="./assets/menuhamburguer.png" alt="Menu">
        </button>
      </div>
 
      <div class="navbar-links" :class="{ 'active': isMenuOpen || !shouldShowIcon }">
        <a href="#home" @click="closeMenu">Home</a>
        <a href="#sobre-mim" @click="closeMenu">Sobre mim</a>
        <a href="#tecnologias" @click="closeMenu">Tecnologias</a>
        <a href="#projetos" @click="closeMenu">Projetos</a>
        <a href="#certificado" @click="closeMenu">Certificado</a>
      </div>
    </nav>
     
     <div id="home">
       <TheComponent1 />
     </div>
     
     <div id="tecnologias">
      
       <TheComponent4 />
     </div>
     
     <div id="sobre-mim">
  
       <TheComponent5 />
     </div>
     
     <div id="projetos">
      
       <TheComponent6 />
     </div>
     
     <div id="certificado">
       <TheComponent7 />
      
     </div>
     <TheComponent3 /> 
   </div>
 </template>
 
 <script>
 import TheComponent1 from './components/TheComponent1.vue';
 import TheComponent3 from './components/TheComponent3.vue';
 import TheComponent4 from './components/TheComponent4.vue';
 import TheComponent5 from './components/TheComponent5.vue';
 import TheComponent6 from './components/TheComponent6.vue';
 import TheComponent7 from './components/TheComponent7.vue';
 
 export default {
   components: {
     TheComponent1,
     TheComponent5,
     TheComponent3,
     TheComponent4,
     TheComponent6,
     TheComponent7,
 },
   data() {
     return {
       isMenuOpen: false,
       shouldShowIcon: window.innerWidth <= 768,
     };
   },
   methods: {
     toggleMenu() {
       this.isMenuOpen = !this.isMenuOpen;
     },
     closeMenu() {
       this.isMenuOpen = false;
     },
     handleResize() {
       this.shouldShowIcon = window.innerWidth <= 768;
     },
   },
   created() {
     window.addEventListener('resize', this.handleResize);
   },
   beforeUnmount() {
     window.removeEventListener('resize', this.handleResize);
   },
 };
 </script>

<style scoped>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
}

html, body {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}
.navbar-links a.router-link-active {
  color: rgb(255, 255, 255);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  border-radius: 10px;
  width: 100%;
  height: 60px;
  position: relative;
  z-index: 5;
  background-color: #000000;
}

.menu-toggle {
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}

.menu-icon {
  width: 30px;
  height: auto;
  display: block;
}

.navbar-links {
  display: flex;
  flex-direction: column;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: #000000;
  border-radius: 10px;
  padding: 50px;
  transform: translateX(-100%);
  transition: transform 0.3s ease-in-out;
  align-items: center;
  justify-content: center;
  overflow-y: auto;
  z-index: 5;
}


.navbar-links.active {
  transform: translateX(0);
}

.navbar-links a {
  font-weight: bold;
  color: #2fff00;
  text-decoration: none;
  margin-bottom: 20px;
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
}

@media (min-width: 769px) {
  /* Estilos para telas maiores */
  nav {
    justify-content: flex-start;
    padding-left: 20px;
  }

  .navbar-links {
    position: static;
    flex-direction: row;
    padding: 0;
    background: none;
    height: auto;
    width: auto;
    transform: translateX(0);
  }

  .navbar-links a {
    margin: 0 10px;
  }
}

@media (max-width: 768px) {
 
  nav {
    width: 100%;
    background: none;
  }

  .navbar-links {
    padding: 20px; 
  }
}

</style>