<template>
  <div class="home">
    <p>Bugun haftaning {{findDay(weekDay)}} kuni!</p>
    <Soat/>
  </div>
  <Monday v-if="weekDay === 4" /> 
  <Tuesday v-if="weekDay === 3" />
  <Friday v-if="weekDay === 5" />
  <Sunday v-if="weekDay ===0" />
  
</template>

<script>
// @ is an alias to /src
import Monday from '@/components/Days/Monday.vue'
import Tuesday from '@/components/Days/Tuesday.vue'
import Friday from '@/components/Days/Friday.vue'
import Sunday from '@/components/Days/Sunday.vue'
import Soat from '@/components/DigitalClock.vue'


export default {
  name: 'HomeView',
  components: {
     Monday,
     Tuesday,
     Friday ,
     Sunday ,
     Soat ,
   },
  
  data(){
    return{
      payshanba : false,
      weekDay:null,
    }
  },
  computed:{
    weekDay(){
      return (new Date().getDay());
    }
  },
  methods:{
    findDay(day){
      let d = '';
      switch (day) {
        case 1: d = "dushanba"; break;
        case 2: d = "seshanba"; break;
        case 3: d = "chorshanba"; break;
        case 4: d = "payshanba"; break;
        case 5: d = "juma"; break;
        case 6: d = "shanba"; break;
      
        default: d = "yakshanba";
          break;
      }
      return d;
    }
  },  
}
</script>

<style>
  p{
    font-weight: bold;
  }

  button{
    padding:10px 20px;
    border: 1px solid black;
    border-radius: 10px;
    font-size: 16px;
  }

  button:hover{
    background: #2c3e50;
    color:#ffff;
    border: 1px solid #fff;
  }
</style>