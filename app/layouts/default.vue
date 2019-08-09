<template>
  <div class="wrapper home">
    <div class="title">
      <p>Takumi's Port</p>
    </div>
    <div class="background" />
    <nuxt />
  </div>
</template>

<style scoped>
.wrapper {
    width: 100vw;
    color: white;
}

.home {
  background-color: black;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color: rgba(255, 255, 255, 0.8);
}

.title {
  position: fixed;
  margin-top: 30vh;
  font-size: 600%;
  opacity: 0.5;
  height: 100vh;
}

.background {
  position: fixed;
  margin-top: 45vh;
  margin-left: 5vw;
  background-image: url('../assets/ruijia-wang-_cX76xaZB5A-unsplash.jpg');
  background-size: cover;
  width: 40vw;
  height: 30vh;
  opacity: 0.5;
}
</style>
