<template>
  <div class="main">
    <div class="top-page">
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
    <div id="contact-me-page" class="contents">
      <contact-me />
    </div>
  </div>
</template>

<script>
import TheTop from '../components/TheTop'
import AboutMe from '../components/AboutMe'
import Languages from '../components/languages/Languages'
import Github from '../components/Github'
import ContactMe from '../components/ContactMe'
export default {
  components: {
    AboutMe,
    TheTop,
    Languages,
    Github,
    ContactMe
  }
}

</script>

<style scoped>
.contents {
  margin-left: auto;
  height: 80vh;
  width: 50vw;
}

.main{
  display: flex;
  flex-direction: column;
}
</style>
