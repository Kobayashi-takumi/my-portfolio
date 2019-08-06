<template>
  <div class="about-me">
    <div class="contents-title">
      About Me
    </div>
    <div class="about-items">
      <ul>
        <li v-for="(item, index) in items" :key="index">
          {{ item.title }}: {{ item.contents }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { title: 'univercity', contents: 'meijigakuin' },
        { title: 'company', contents: 'HC assert manegement' }
      ]
    }
  }
}
</script>

<style scoped>
.about-me {
    display: flex;
    flex-direction: column;
    height: 100vh;
    font-style: italic;
    background-color: rgba(255, 255, 255, 0.1);
}

.contents-title {
    margin-right: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(250, 134, 1);
    font-size: 500%;
    margin-top: 5vh;
    margin-left: 5vw;
}

.about-items {
    margin-top: 50vh;
    margin-left: auto;
    margin-right: 5vw;
    font-size: 30px;
}
</style>
