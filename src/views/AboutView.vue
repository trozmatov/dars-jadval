<template>

  <div class="about">
    <h1>Kurslar</h1>
  </div>
  <div>
    <button @click="handleSubjects('tarix')">Tarix</button>
    <button @click="handleSubjects('kimyo')">Kimyo</button>
    <button @click="handleSubjects('bio')">Biologiya</button>
    <button @click="handleSubjects('math')">Matematika</button>
    <button @click="handleSubjects('front')">Front-end dasturlash</button>
    <button @click="handleSubjects('russianBig')">Rus tili</button>
    <button @click="handleSubjects('russianLO')">Bolalar uchun rus tili (1-guruh)</button>
    <button @click="handleSubjects('russianLT')">Bolalar uchun rus tili (2-guruh)</button>
  </div>
  <History  v-if="tarix" />
  <Kimyo v-if="kimyo"  />
  <Biology v-if="bio"  />
  <Matem v-if="math" />
  <Frontend  v-if="front" />
  <RussianBig v-if="russianBig" />
  <RussianLittleOne v-if="russianLO"/>
  <RussianLittleTwo v-if="russianLT" />

</template>
<script>
  import History from '@/components/Courses/History.vue'
  import Biology from '@/components/Courses/Biology.vue'
  import Matem from '@/components/Courses/Matem.vue'
  import Kimyo from '@/components/Courses/Kimyo.vue'
  import Frontend from '@/components/Courses/Frontend.vue'
  import RussianBig from '@/components/Courses/RussianBig.vue'
  import RussianLittleOne from '@/components/Courses/RussianLittleOne.vue'
  import RussianLittleTwo from '@/components/Courses/RussianLittleTwo.vue'


export default {
  components:{
    History, Biology , Matem , Kimyo ,  Frontend , RussianBig , RussianLittleOne , RussianLittleTwo
  },

  data(){
    return{
      tarix:false,
      kimyo: false,
      bio:false,
      math:false,
      front: false,
      russianBig: false ,
      russianLO: false ,
      russianLT: false

    }
    
  },
  
  methods:{
    handleSubjects(val){
      this.tarix = false
      this.kimyo = false
      this.bio = false
      this.math = false
      this.front = false
      this.russianBig = false
      this.russianLO = false
      this.russianLT = false

      if(val == 'tarix') this.tarix = true;
      if(val == 'kimyo') this.kimyo = true;
      if(val == 'bio') this.bio = true;
      if(val == 'math') this.math = true;
      if(val == 'front') this.front = true;
      if(val == 'russianBig') this.russianBig = true;
      if(val == 'russianLO') this.russianLO = true;
      if(val == 'russianLT') this.russianLT = true;

    }
  },
}

</script>

<style>
button{
  margin: 5px;
}

</style>