<template>
  <div class="language">
    <div class="contents-title">
      Languages
    </div>
    <div v-if="!contentsDetail" class="langeges-contents" :class="{ deactive: classActive}">
      <div class="front">
        <p class="front-title" @mouseover="frontActive" @mouseleave="frontDeactive" @click="detailOn">
          Front End
        </p>
        <div v-if="frontShow" class="clicks front-click">
          <p><i class="el-icon-d-arrow-left" />click!!</p>
        </div>
      </div>
      <div class="server">
        <p class="server-title" @mouseover="serverActive" @mouseleave="serverDeactive">
          Server Side
        </p>
        <div v-if="serverShow" class="clicks server-click">
          <p>click!!<i class="el-icon-d-arrow-right" /></p>
        </div>
      </div>
    </div>
    <div v-else class="contents-detail langeges-contents">
      <div class="card">
        <i class="el-icon-d-arrow-left" @click="detailOff" />
        <p>detail</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      frontShow: false,
      serverShow: false,
      contentsDetail: false,
      classActive: false
    }
  },
  methods: {
    frontActive () {
      this.frontShow = true
    },
    frontDeactive () {
      this.frontShow = false
    },
    serverActive () {
      this.serverShow = true
    },
    serverDeactive () {
      this.serverShow = false
    },
    detailOn () {
      this.contentsDetail = true
      this.frontShow = false
      this.classActive = true
    },
    detailOff () {
      this.contentsDetail = false
    }
  }
}
</script>

<style scoped>
.language {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

.contents-title {
    margin-left: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(250, 134, 1);
    font-size: 500%;
    padding-top: 5vh;
    padding-right: 5vw;
    height: 20vh;
    font-style: italic;
}

.langeges-contents {
  height: 80vh;
  display: flex;
  flex-direction: column;
}

.front {
  margin-right: auto;
  margin-left: 5vw;
  margin-top: 10vh;
  display: flex;
  align-items: center;
  transform: rotate(5deg);
}

.front-title {
  color: rgba(0, 0, 0, 0);
  -webkit-text-stroke: 1px rgb(255, 255, 255);
  font-size: 500%;
}

.front-title:hover {
  animation: mouse-over 1s ease infinite;
  border: 1px solid rgb(14, 172, 0);
}

.server {
  margin-top: auto;
  margin-left: auto;
  margin-right: 5vw;
  margin-bottom: 10vh;
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
  transform: rotate(-5deg);
}

.server-title {
  color: rgba(0, 0, 0, 0);
  -webkit-text-stroke: 1px rgb(255, 255, 255);
  font-size: 500%;
}

.server-title:hover {
  animation: mouse-over2 1s ease infinite;
  border: 1px solid rgb(250, 134, 1);
}

.clicks {
  font-size: 300%;
  margin-left: 5vw;
  margin-right: 5vh;
}

.front-click {
  color: rgba(14, 172, 0, 0.8);
}

.server-click {
  color: rgba(250, 134, 1, 0.8);
}

@keyframes mouse-over {
  0% {
    -webkit-text-stroke: 1px #ffff;
  }
  50% {
    -webkit-text-stroke: 1px rgb(14, 172, 0);
    color: rgb(14, 172, 0);
  }
  100% {
    -webkit-text-stroke: 1px #ffff;
  }
}

@keyframes mouse-over2 {
  0% {
    -webkit-text-stroke: 1px #ffff;
  }
  50% {
    -webkit-text-stroke: 1px rgb(250, 134, 1);
    color: rgb(250, 134, 1);
  }
  100% {
    -webkit-text-stroke: 1px #ffff;
  }
}

@keyframes page-in {
  0% {
    background: rgb(14, 172, 0);
    width: 100%;
    z-index: 1;
  }
  100% {
    width: 0;
  }
}

@keyframes page-out {
  0% {
    opacity: 1;
  }
  50% {
    margin-left: 50vw;
  }
  100% {
    margin-left: auto;
    opacity: 0;
  }
}

@keyframes page-opacity {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.deactive {
  animation: page-out 3s;
}

.contents-detail {
  justify-content: center;
  align-items: center;
  position: relative;
}

.contents-detail::after {
  content: '';
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  animation: page-in 3s ease;
}

.card {
  animation: page-opacity 4s;
}
</style>
