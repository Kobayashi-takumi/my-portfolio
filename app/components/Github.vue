<template>
  <div class="github">
    <div class="contents-title">
      Github
    </div>
    <div class="github-contents">
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
    height: 100%;
    font-style: italic;
}

.contents-title {
    margin-right: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(219, 124, 15);
    font-size: 500%;
    margin-top: 5%;
    margin-left: 5%;
    height: 15%;
}

.github-contents {
    height: 80%;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-end;
}

.btn:hover::before {
  content: 'Click';
  font-size: 5em;
  color: rgb(14, 172, 0);
  border-bottom: 1px solid rgb(14, 172, 0);
}

.btn {
    height: 30%;
    width: 50%;
    min-width: 300px;
    background-image: url('../assets/Octocat.png');
    border-radius: 10px;
    margin-bottom: 3%;
    background-color: rgba(255, 255, 255, 0.8);
    animation: git 3s ease 0s infinite;
    text-decoration: none;
}

@keyframes git {
    0% {
        width: 50%;
    }
    50% {
        width: 40%;
    }
    100% {
        width: 50%;
    }
}

</style>
