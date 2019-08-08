<template>
  <div class="language">
    <div class="contents-title">
      Languages
    </div>
    <div v-if="!contentsDetail" class="langeges-contents">
      <div class="front">
        <p class="front-title" @mouseover="frontActive" @mouseleave="frontDeactive" @click="detailOn(0)">
          Front End
        </p>
        <div v-if="frontShow" class="clicks front-click">
          <p><i class="el-icon-d-arrow-left" />click!!</p>
        </div>
      </div>
      <div class="server">
        <p class="server-title" @mouseover="serverActive" @mouseleave="serverDeactive" @click="detailOn(1)">
          Server Side
        </p>
        <div v-if="serverShow" class="clicks server-click">
          <p>click!!<i class="el-icon-d-arrow-right" /></p>
        </div>
      </div>
    </div>
    <div v-else class="detail">
      <detail @detail-off="detailOff" />
    </div>
  </div>
</template>

<script>
import detail from './detail'
export default {
  components: {
    detail
  },
  data () {
    return {
      frontShow: false,
      serverShow: false,
      contentsDetail: false
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
    detailOn (id) {
      this.contentsDetail = true
      this.$store.commit('setLanguages', id)
      this.frontShow = false
      this.serverShow = false
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
    height: 100%;
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

.langeges-contents {
  height: 80%;
  display: flex;
  flex-direction: column;
}

.front {
  margin-right: auto;
  margin-left: 5%;
  margin-top: 10%;
  display: flex;
  align-items: center;
}

.front-title {
  color: rgb(255, 255, 255);
  font-size: 400%;
}

.front-title:hover {
  animation: mouse-over 1s ease infinite;
  border: 1px solid rgb(14, 172, 0);
  color: rgba(0, 0, 0, 0);
  -webkit-text-stroke: 1px rgb(255, 255, 255);
}

.server {
  margin-top: auto;
  margin-left: auto;
  margin-right: 5%;
  margin-bottom: 10%;
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
}

.server-title {
  color: rgb(255, 255, 255);
  font-size: 400%;
}

.server-title:hover {
  animation: mouse-over2 1s ease infinite;
  border: 1px solid rgb(250, 134, 1);
  color: rgba(255, 255, 255, 0);
  -webkit-text-stroke: 1px rgb(255, 255, 255);
}

.clicks {
  font-size: 300%;
  margin-left: 5%;
  margin-right: 5%;
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

.detail {
  height: 100%;
}

</style>
