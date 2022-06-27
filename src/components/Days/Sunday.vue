<template>
  <div id="table">
    <h2>Yakshanba kuni uchun darslar jadvali:</h2>
    <table>
        <tr>
            <th>Fan</th>
            <th>Darsning boshlanish vaqti</th>
            <th>Xona</th>
            <th>Holati</th>
        </tr>
        <tr>
            <td>Kompyuter asoslari</td>
            <td>10:00</td>
            <td>3-xona</td>
            <td>{{statusBar(findClock)}}</td>
        </tr>
        <tr>
            <td>Arab tili</td>
            <td>10:00</td>
            <td>4-xona</td>
            <td>{{statusBar(findClock)}}</td>
        </tr>
        <tr>
            <td>Arab tili</td>
            <td>14:00</td>
            <td>4-xona</td>
            <td>{{statusBar(findClock)}}</td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
    name: 'Sunday',
    data(){
        return{
        status:null ,
        findClock:null
        }
        

    },
    conputed:{
        findClock (){
            return (new Date().getHours());
        }
    },
    methods:{
        statusBar(clock){
           let text= "";
           switch(clock){
            case 9 : text = 'Dars boshlanishiga 1 soatdan kam vaqt qoldi'; break;
            case 10: text = 'Dars boshlandi'; break;
            case 13 : text = 'Dars boshlanishiga 1 soatdan kam vaqt qoldi'; break;
            case 14: text = 'Dars boshlandi'; break;

            default: text = 'Dars tugadi';
                break;

            

           }

           return text;
        }
    }
}
</script>

<style>
#table{
    margin: 20px;
}
table{
    margin: 0 auto;
}

th , td , table{
    border:1px solid;
}

th , td {
    padding:10px;
}
</style>