<template>
  <div class="detail">
    <div class="back-btn" @click="detailOff">
      <i class="el-icon-d-arrow-left" />
    </div>
    <div class="detail-contents">
      <div v-for="(item, index) in languages[languageId]" :key="index" class="languages">
        <div class="title">
          {{ item.language }}
        </div>
        <div class="year">
          year: {{ item.year }}
        </div>
        <div v-for="(fwItem, id) in item.framework" :key="id" class="flameworks">
          {{ fwItem }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      languages: [
        [
          { language: 'HTML', year: '1年', framework: [] },
          { language: 'CSS', year: '1年', framework: ['Sass'] },
          { language: 'javascript', year: '1年', framework: ['Vue.js (Nuxt.js)', 'React'] }
        ],
        [
          { language: 'Python', year: '1年', framework: ['Django', 'Flask'] },
          { language: 'Node.js (javascript)', year: '1月', framework: ['Express'] }
        ]
      ],
      languageId: ''
    }
  },
  created () {
    this.languageId = this.$store.state.languages
  },
  methods: {
    detailOff () {
      this.$emit('detail-off')
    }
  }
}
</script>

<style scoped>

.detail {
  display: flex;
  width: 100%;
  height: 80%;
  position: relative;
  justify-content: center;
  animation: page-in 3s ease;
}

.back-btn {
    width: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 300%;
}

.back-btn:hover::after {
    content: 'Back';
    font-size: 3em;
    opacity: 0.3;
    animation: back-font 1s ease infinite;
}

.back-btn:hover {
    animation: mouse-over 1s ease infinite;
    background: rgba(14, 172, 0, 0.1);
    height: 80%;
}

.detail-contents {
    width: 80%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.languages {
    margin-top: 3%;
    margin-left: 3%;
    display: flex;
    flex-direction: column;
}

.title {
    font-size: 18px;
    border-bottom: 1px solid #ffff;
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

@keyframes back-font {
    0% {
    width: 0%;
  }
  100% {
    width: 50%;
  }
}

@keyframes page-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

/*
.detail::after {
  content: '';
  width: 50%;
  height: 80%;
  position: absolute;
  top: 0;
  right: 0;
  z-index: -1;
  animation: page-in 3s ease;
}

.detail::before {
  content: '';
  width: 50%;
  height: 80%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  animation: page-in 3s ease;
}

@keyframes page-in {
  0% {
    background: rgb(14, 172, 0);
    width: 50%;
    z-index: 999;
  }
  100% {
    width: 0%;
  }
}

*/
</style>
