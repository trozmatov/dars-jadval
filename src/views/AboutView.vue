<template>

  <div class="about">
    <h1>Kurslar</h1>
  </div>
  <div>
    <button @click="handleSubjects('tarix')">Tarix</button>
    <button @click="handleSubjects('kimyo')">Kimyo</button>
    <button @click="handleSubjects('bio')">Biologiya</button>
    <button @click="handleSubjects('math')">Matematika</button>
  
  </div>
  <History  v-if="tarix" />
  <Kimyo v-if="kimyo"  />
  <Biology v-if="bio"  />
  <Matem v-if="math" />

</template>
<script>
  import History from '@/components/Courses/History.vue'
  import Biology from '@/components/Courses/Biology.vue'
  import Matem from '@/components/Courses/Matem.vue'
  import Kimyo from '@/components/Courses/Kimyo.vue'


export default {
  components:{
    History, Biology , Matem , Kimyo
  },

  data(){
    return{
      tarix:false,
      kimyo: false,
      bio:false,
      math:false,

    }
    
  },
  
  methods:{
    handleSubjects(val){
      this.tarix = false
      this.kimyo = false
      this.bio = false
      this.math = false

      if(val == 'tarix') this.tarix = true;
      if(val == 'kimyo') this.kimyo = true;
      if(val == 'bio') this.bio = true;
      if(val == 'math') this.math = true;

    }
  },
}

</script>

<style>
button{
  margin: 5px;
}

</style>