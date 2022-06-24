<template>
  <div id="table">
    <h2>Seshanba</h2>
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
    </table>
  </div>
</template>

<script>
export default {
    name: 'Tuesday',
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
</style>