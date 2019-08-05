<template>
  <div class="wrapper container">
    <div class="title">
      <p>Takumi's Port</p>
    </div>
    <div class="header">
      <p class="header-item">
        About me
      </p>
      <p class="header-item">
        Langages
      </p>
      <p class="header-item">
        Github
      </p>
      <p class="header-item">
        Contact me
      </p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 20vw;
    background: rgba(255, 255, 255, 0.1);
}

.header-item {
    margin: 3px;
    border-bottom: 1px solid #ffff;
    margin-top: 5vh;
}

.container {
    display: flex;
    flex-direction: row;
    height: 100vh;
}

.title {
    width: 80vw;
    text-align: center;
    margin-top: 50vh;
}

</style>
