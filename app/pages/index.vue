<template>
  <div>
    <div class="contents">
      <the-top />
    </div>
    <div id="about" class="contents">
      <about-me />
    </div>
    <div id="languages" class="contents">
      <languages />
    </div>
    <div id="github-page" class="contents">
      <github />
    </div>
  </div>
</template>

<script>
import TheTop from '../components/TheTop'
import AboutMe from '../components/AboutMe'
import Languages from '../components/Languages'
import Github from '../components/Github'
export default {
  components: {
    AboutMe,
    TheTop,
    Languages,
    Github
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
