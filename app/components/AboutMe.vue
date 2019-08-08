<template>
  <div class="about-me">
    <div class="contents-title">
      About Me
    </div>
    <div class="about-items">
      <div class="items">
        <div class="self-introduction">
          <p>About</p>
          <ul>
            <li>Name: {{ introduction.name }}</li>
            <li>Birthday: {{ introduction.birthday }}</li>
            <li>From: {{ introduction.birthPlace }}</li>
          </ul>
        </div>
      </div>
      <div class="items">
        <div class="career">
          <p>Career</p>
          <ul>
            <li v-for="(career, index) in careers" :key="index">
              {{ career.year }}: {{ career.contents }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      introduction: {
        name: '小林　拓己',
        birthday: '1995-10-29',
        birthPlace: '神奈川県藤沢市'
      },
      careers: [
        { year: 2014, contents: 'Meijigakuin University' },
        { year: 2018, contents: 'HC assert manegement' }
      ]
    }
  }
}
</script>

<style scoped>
.about-me {
    display: flex;
    flex-direction: column;
    height: 100%;
}

.contents-title {
    margin-right: auto;
    color: rgba(0, 0, 0, 0);
    -webkit-text-stroke: 1px rgb(250, 134, 1);
    font-size: 500%;
    margin-top: 5%;
    margin-left: 5%;
    font-style: italic;
}

.about-items {
    display: flex;
    width: 100%;
    height: 100%;
}

.items {
  width: 50%;
  color: #ffff;
  font-size: 24px;
  margin: 3%;
  display: flex;
}

.self-introduction {
  margin-top: 3%;
  margin-left: 3%;
}

.career {
  margin-top: auto;
  margin-left: auto;
  margin-bottom: 3%;
  margin-right: 3%;
}
</style>
