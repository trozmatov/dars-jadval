<template>
  <h1>Courses</h1>
  <div>
    <form @submit.prevent="courseSelect">
      <select v-model="selected">
        <option v-for="(subject, index) in subjects" :key="index">
          {{ subject.course }}
        </option>
      </select>
      <h2>{{ selected }}</h2>
    </form>
  </div>
  <div v-if="selected === 'Rus tili'">
    <button @click="handleSubjects('russianBig')">Rus tili</button>
    <button @click="handleSubjects('russianLO')">
      Bolalar uchun rus tili (1-guruh)
    </button>
    <button @click="handleSubjects('russianLT')">
      Bolalar uchun rus tili (2-guruh)
    </button>
  </div>
  <div v-if="selected === 'Tarix'">
    <button @click="handleSubjects('tarix')">Dars jadvali</button>
  </div>
  <div v-if="selected === 'Frontend dasturlash'">
    <button @click="handleSubjects('front')">Dars jadvali</button>
  </div>
  <div v-if="selected === 'Biologiya'">
    <button @click="handleSubjects('bio')">Dars jadvali</button>
  </div>
  <div v-if="selected === 'Kimyo'">
    <button @click="handleSubjects('kimyo')">Dars jadvali</button>
  </div>
  <div v-if="selected === 'Bolalar uchun ingliz tili'">
    <button @click="handleSubjects('englishM0')">Birinchi guruh</button>
    <button @click="handleSubjects('englishM1')">Ikkinchi guruh</button>
    <button @click="handleSubjects('englishM2')">Uchinchi guruh</button>
  </div>
  <div v-if="selected === 'Ingliz tili'"></div>

  <History v-if="tarix" />
  <Kimyo v-if="kimyo" />
  <Biology v-if="bio" />
  <Matem v-if="math" />
  <Frontend v-if="front" />
  <RussianBig v-if="russianBig" />
  <RussianLittleOne v-if="russianLO" />
  <RussianLittleTwo v-if="russianLT" />
  <EnglishM0 v-if="englishM0" />
  <EnglishM1 v-if="englishM1" />
  <EnglishM2 v-if="englishM2" />
</template>

<script>
import History from "@/components/Courses/History.vue";
import Biology from "@/components/Courses/Biology.vue";
import Matem from "@/components/Courses/Matem.vue";
import Kimyo from "@/components/Courses/Kimyo.vue";
import Frontend from "@/components/Courses/Frontend.vue";
import RussianBig from "@/components/Courses/RussianBig.vue";
import RussianLittleOne from "@/components/Courses/RussianLittleOne.vue";
import RussianLittleTwo from "@/components/Courses/RussianLittleTwo.vue";
import EnglishM0 from "@/components/Courses/EnglishM0.vue";
import EnglishM1 from "@/components/Courses/EnglishM1.vue";
import EnglishM2 from "@/components/Courses/EnglishM2.vue";

export default {
  components: {
    History,
    Biology,
    Matem,
    Kimyo,
    Frontend,
    RussianBig,
    RussianLittleOne,
    RussianLittleTwo,
    History,
    EnglishM0,
    EnglishM1,
    EnglishM2,
  },

  data() {
    return {
      tarix: false,
      kimyo: false,
      bio: false,
      math: false,
      front: false,
      russianBig: false,
      russianLO: false,
      russianLT: false,
      englishM0: false,
      englishM1: false,
      englishM2: false,
      subjects: [
        { course: "Tarix" },
        { course: "Ingliz tili" },
        { course: "Bolalar uchun ingliz tili" },
        { course: "Rus tili" },
        { course: "Frontend dasturlash" },
        { course: "Biologiya" },
        { course: "Kimyo" },
        { course: "Arab tili" },
      ],

      selected: null,
    };
  },

  methods: {
    handleSubjects(val) {
      this.tarix = false;
      this.kimyo = false;
      this.bio = false;
      this.math = false;
      this.front = false;
      this.russianBig = false;
      this.russianLO = false;
      this.russianLT = false;
      this.englishM0 = false;
      this.englishM1 = false;
      this.englishM2 = false;

      if (val == "tarix") this.tarix = true;
      if (val == "kimyo") this.kimyo = true;
      if (val == "bio") this.bio = true;
      if (val == "math") this.math = true;
      if (val == "front") this.front = true;
      if (val == "russianBig") this.russianBig = true;
      if (val == "russianLO") this.russianLO = true;
      if (val == "russianLT") this.russianLT = true;
      if (val == "englishM0") this.englishM0 = true;
      if (val == "englishM1") this.englishM1 = true;
      if (val == "englishM2") this.englishM2 = true;
    },
  },
  courseSelect() {
    console.log("click");
  },
};
</script>

<style>
select {
  position: relative;
  display: block;
  width: 70%;
  margin: 0 auto;
  font-family: "Open Sans", "Helvetica Neue", "Segoe UI", "Calibri", "Arial",
    sans-serif;
  font-size: 18px;
  color: #60666d;
  
}
</style>
