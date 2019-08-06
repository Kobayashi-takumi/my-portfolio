<template>
  <div class="github">
    <div class="contents-title">
      Github
    </div>
    <div class="github-contents">
      <div class="btn-title">
        <i class="el-icon-bottom" />Click
      </div>
      <a href="https://github.com/Kobayashi-takumi" class="btn" />
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.github {
    display: flex;
    flex-direction: column;
    height: 100vh;
    font-style: italic;
    background-color: rgba(255, 255, 255, 0.1);
}

.contents-title {
    margin-right: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(219, 124, 15);
    font-size: 500%;
    margin-top: 5vh;
    margin-left: 5vw;
    height: 15vh;
}

.github-contents {
    height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-end;
}

.btn-title {
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(255, 255, 255);
    font-size: 400%;
    margin-right: 5vw;
}

.btn {
    height: 30vh;
    width: 50vw;
    min-width: 300px;
    background-image: url('../assets/Octocat.png');
    border-radius: 10px;
    margin-bottom: 3vh;
    background-color: rgba(255, 255, 255, 0.8);
    animation: git 3s ease 0s infinite;
}

@keyframes git {
    0% {
        width: 50vw;
    }
    50% {
        width: 40vw;
    }
    100% {
        width: 50vw;
    }
}

</style>
