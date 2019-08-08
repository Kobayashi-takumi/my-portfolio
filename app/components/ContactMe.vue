<template>
  <div class="contact-me">
    <div class="contents-title">
      Contact Me
    </div>
    <div class="contact-contents">
      <div class="message">
        <p>
          <span
            v-for="(t, index) in text"
            :key="index"
            class="item"
            :style="{animationDelay: index*100+'ms'}"
            v-text="t"
          />
        </p>
      </div>
      <div class="e-mail">
        <a href="mailto:takumi.kobayashi.devlopment@gmail.com" class="link"><i class="el-icon-right" />takumi.kobayashi.devlopment@gmail.com</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      text: 'Please give me a job!!'
    }
  }
}
</script>

<style scoped>
.contact-me {
    display: flex;
    flex-direction: column;
    height: 100%;
    font-style: italic;
}

.contents-title {
    margin-left: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(250, 134, 1);
    font-size: 500%;
    padding-top: 5%;
    padding-right: 5%;
    height: 20%;
    font-style: italic;
}

.contact-contents {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100%;
}

.message {
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(255, 255, 255);
    font-size: 300%;
}

.e-mail {
    font-size: 200%;
    margin-top: 3%;
    margin-left: auto;
    margin-right: 3%;
}

.link {
  text-decoration: none;
  color: #ffff;
  border-bottom: 1px solid #ffff;
}

@keyframes text-in {
  0% {
    transform: translate(0, -20px);
    opacity: 0;
    color: rgb(14, 172, 0);
  }
}

.item {
  animation: text-in 3s cubic-bezier(0.22, 0.15, 0.25, 1.43) 0s backwards infinite;
}
</style>
