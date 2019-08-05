<template>
  <div>
    <div class="contents">
      <the-top />
    </div>
    <div class="contents">
      <about-me />
    </div>
  </div>
</template>

<script>
import TheTop from '../components/TheTop'
import AboutMe from '../components/AboutMe'
export default {
  components: {
    AboutMe,
    TheTop
  }
}
</script>

<style scoped>
.contents {
  height: 100vh;
}

.page {
  width: 100vw;
}
</style>
