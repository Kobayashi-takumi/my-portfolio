<template>
  <div class="about-me">
    <div class="contents-title">
      <p>About Me</p>
    </div>
    <div class="about-items">
      <li>
        <ul v-for="(item, index) in items" :key="index">{{ item.title }}: {{ item.contents }}</ul>
      </li>
    </div>
  </div>
</template>

<script>
export default {
  asyncData () {
    return {
      items: [
        { title: 'univercity', contents: 'meijigakuin' },
        { title: 'company', contetnts: 'HC assert manegement' }
      ]
    }
  }
}
</script>

<style scoped>
.about-me {
    display: flex;
    flex-direction: column;
}

.contents-title {
    margin-top: 10vh;
    background-color: rgba(255, 255, 255, 0.8);
    width: 50vw;
}
</style>
