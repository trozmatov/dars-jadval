<template>
  <div id="table">
    <h2>Juma kuni uchun darslar jadvali</h2>
    <table>
        <tr>
            <th>Fan</th>
            <th>Darsning boshlanish vaqti</th>
            <th>Xona</th>
            <th>O'qituvchi</th>
        </tr>
        <tr>
            <td>Rus tili</td>
            <td>07:30</td>
            <td>2-xona</td>
            <td>Rahbaroy opa</td>
        </tr>
        <tr>
            <td>Ingliz tili</td>
            <td>08:00</td>
            <td>3-xona</td>
            <td>Mavluda</td>
        </tr>
        <tr>
            <td>Ingliz tili</td>
            <td>09:00</td>
            <td>4-xona</td>
            <td>Mabrura opa</td>
        </tr>
        <tr>
            <td>Arab tili</td>
            <td>08:00</td>
            <td>3-xona</td>
            <td>Nuriddin aka</td>
        </tr>
        <tr>
            <td>Arab tili</td>
            <td>10:00</td>
            <td>3-xona</td>
            <td>Nuriddin aka</td>
        </tr>
        <tr>
            <td>Ingliz tili</td>
            <td>08:00</td>
            <td>3-xona</td>
            <td>Mavluda</td>
        </tr>
    </table>
    
  </div>
  <a 
    href="https://docs.google.com/forms/d/e/1FAIpQLSfbrfdAXa3qzGGeJ8IfnDAXQUHD16ZQ8LSH6A7dVaKXDbFhGw/viewform?usp=sf_link"
    > 
    Shikoyat qoldirish
    </a>  
</template>

<script>
export default {
    name: 'Thursday',
    props:[

    ]
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

.copy{
    font-weight: normal;
}

a{
    text-decoration: none;
    color:#414f5d;
    padding: 10px 20px;
    border: 1px solid black;
    background: rgb(242, 227, 227);
    border-radius: 10px;
    
}
</style>