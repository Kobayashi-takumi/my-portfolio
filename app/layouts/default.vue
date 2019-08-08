<template>
  <div class="wrapper home">
    <div class="title">
      <p>Takumi's Port</p>
    </div>
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
</style>
