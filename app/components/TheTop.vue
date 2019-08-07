<template>
  <div class="wrapper container">
    <div class="title">
      <p>Takumi's Port</p>
    </div>
    <div v-if="isShow === false" v-cloak class="menu-btn">
      <i class="el-icon-menu" @mouseover="isActive" />
    </div>
    <div v-if="isShow" class="header">
      <div class="heder-btn">
        <i class="el-icon-close" @mouseover="isActive" />
      </div>
      <div class="header-items">
        <p class="header-item">
          <nuxt-link v-scroll-to="'#about'" to>
            About me
          </nuxt-link>
        </p>
        <p class="header-item">
          <nuxt-link v-scroll-to="'#languages'" to>
            Langages
          </nuxt-link>
        </p>
        <p class="header-item">
          <nuxt-link v-scroll-to="'#github-page'" to>
            Github
          </nuxt-link>
        </p>
        <p class="header-item">
          Contact me
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isShow: false
    }
  },
  methods: {
    isActive () {
      this.isShow = !this.isShow
    }
  }
}
</script>

<style scoped>
a {
  color: #ffff;
}

.header {
    display: flex;
    flex-direction: row;
    width: 40vw;
    background: rgba(255, 255, 255, 0.1);
    transition: fadeIn 1s ease;
}

.header-items {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.header-item {
    margin-top: 10px;
}

.header-btn {
  margin-bottom: auto;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  width: 20%;
}

.container {
    display: flex;
    flex-direction: row;
    height: 100vh;
}

.title {
    width: 100vw;
    text-align: center;
    margin-top: 50vh;
}

.menu-btn {
  margin-left: auto;
  margin-bottom: auto;
  margin-right: 1vw;
}

i {
  font-size: 30px;
}

i:hover {
  opacity: 0.5;
}

@keyframes fadeIn {
  0% {opacity: 0;}
  100% {opacity: 1;}
}
</style>
