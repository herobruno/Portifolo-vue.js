<template>
  <div>
    <div
      class="background"
      :style="{ 'background-image': 'url(' + currentGifUrl + ')' }"
    />
    <div class="container">
      <div class="content">
        <button @click="changeBackground">
          Animated Mode
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheComponent3',
  data() {
    return {
      gifs: [
        require('@/assets/background1.gif'),
        require('@/assets/background2.gif'),
        require('@/assets/background3.gif'),
      ],
      currentGifIndex: 0,
      currentGifUrl: require('@/assets/background1.gif'),
    }
  },
  methods: {
    changeBackground() {
      const newIndex = (this.currentGifIndex + 1) % this.gifs.length
      this.currentGifIndex = newIndex
      this.currentGifUrl = this.gifs[newIndex]
    },
  },
}
</script>

<style scoped>
html, body {
  overflow-x: hidden;
}
.container {
  position:absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 54px;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
  margin-bottom: 16%
  
   
}

.background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  z-index: -5;
  
  
  

}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: rgb(234, 20, 20);

}

button {
  position: absolute;
  background-color: rgb(0, 0, 0);
  color: rgb(255, 255, 255);
  font-size: 1.5rem;
  border-radius: 10px;
  cursor: pointer;
  bottom: -500px;
  font-family:Arial, Helvetica, sans-serif;

  
}
@media screen and (max-width: 575px) and (min-width: 320px) {
  button {
    position: fixed;
    bottom: 1px; 
    left: 50px; 
    width: 70%;
    height: 30px;
    margin: 0; 
    
  }
}


@media screen and (min-width: 576px) and (max-width: 1899px) {
  button {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 40px;
    margin: 0;
  }
}



</style>