<template>
  <div class="certificates-carousel">
    <h1>Certificados</h1>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div
          v-for="(certificate, index) in certificates"
          :key="index"
          class="swiper-slide"
        >
          <div class="certificate-frame">
            <img :src="require(`@/assets/${certificate.image}`)" :alt="certificate.title">
          </div>
          <p>{{ certificate.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';

export default {
  data() {
    return {
      certificates: [
        {
         
          description: 'HTML5 & CSS3',
          image: '74728632.jpg'
        },
        {
     
          description: 'NODE.JS',
          image: '81743696.jpg'
        },
        {
        
          description: 'TYPE SCRIPT',
          image: '98240228.jpg'
        },
        
      ],
    };
  },
  mounted() {
    new Swiper('.swiper-container', {
      slidesPerView: 2,
      spaceBetween: 20,
    });
  },
};
</script>

<style scoped>
html, body {
  overflow-x: hidden;
}
.certificates-carousel {
  display: flex;
  flex-direction: column;
  text-align: center;
  width: 100%;
  max-width: 950px; 
  margin: 0 auto; 
  overflow: hidden; 
  
}

h1 {
  font-size: 24px;
  margin-bottom: 20px;
  color: rgb(0, 255, 0);
  text-align: left;
  font-family:Arial, Helvetica, sans-serif;
}

.swiper-container {
  width: 90%;
  padding: 10px
 
}

.swiper-slide {

  border-radius: 5px;
  padding: 20px;
  text-align: center;
  width: 450px;
  box-shadow: 0px 0px 5px 4px rgb(0, 0, 0);
}

.certificate-frame {
  text-align: center;
  margin-bottom: 10px;
}

.certificate-frame img {
  max-width: 90%;
  max-height: 200%;
  border-radius: 2%;
  box-shadow: 0px 0px 10px  rgb(38, 255, 0);
}

h2 {
  font-size: 18px;
  margin-bottom: 10px;
  font-family:Arial, Helvetica, sans-serif;
  color: white;
  
  
}

p {
  font-size: 14px;
  font-family:Arial, Helvetica, sans-serif;
  color: rgb(0, 255, 26);
  
}


</style>