<template>
  <div class="hello">
    <h1>{{ mensaje }}</h1>
    <div id="app" class="container-fluid d-flex justify-content-center align-items-center">

        <table id="customers" class="w-50">
            <tr>
                <th v-for='head in dataHeaders' :key="head">{{head}}</th>
            </tr>

            <tr v-for='user in usuarios' :key="user">
                <td>{{user.id}}</td>
                <td> {{user.nombre}} </td>
                <td>{{user.apellido}}</td>
                <td> {{user.run}}</td>
                <td> {{user.nacimiento}}</td>
                <td> {{user.edad}}</td>

            </tr>
        </table>
    
  </div>
  </div>
</template>

<script>
export default {
  name: 'DataTable',
  data(){
      return{
          
        dataHeaders: ['#', 'Nombre', 'Apellido', 'RUN', 'Nacimiento', 'Edad'],
        usuarios: [{
                id: 1,
                nombre: 'Roberto',
                apellido: 'Gomez',
                run: '12345678-9',
                nacimiento: '12/05/87',
                edad: 34
            },
            {
                id: 2,
                nombre: 'Daniel',
                apellido: 'Rivas',
                run: '1238445678-1',
                nacimiento: '02/08/94',
                edad: 27
            },
            {
                id: 3,
                nombre: 'Victor',
                apellido: 'Hugo',
                run: '1234534-k',
                nacimiento: '12/05/77',
                edad: 55
            }
        ]
    }
      
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#customers {
  font-family: Arial, Helvetica, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

#customers td, #customers th {
  border: 1px solid #ddd;
  padding: 8px;
}

#customers tr:nth-child(even){background-color: #f2f2f2;}

#customers tr:hover {background-color: #ddd;}

#customers th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: left;
  background-color: #4CAF50;
  color: white;
}
</style>
