<template>
  <div class="rebounding-table">
    <table>
      <thead>
        <tr><th colspan="3">籃板</th></tr>
      </thead>
      <tbody>
        <tr v-for="content in contents" :key="content.id">
          <td>{{ content.rank }}</td>
          <td>
            <p>{{ content.player }}</p>
            <p>{{ content.departement}}</p>
          </td>
          <td>{{ content.rebounding }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup() {
    const contents = reactive([
      {id: 1, rank: 1,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 2, rank: 2,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 3, rank: 3,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 4, rank: 4,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 5, rank: 5,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 6, rank: 6,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 7, rank: 7,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 8, rank: 8,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 9, rank: 9,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
      {id: 10, rank: 10,player:"徐聖哲" ,departement:"資工" ,rebounding:"10"},
    ])
    return { contents }
  }
}
</script>

<style scoped>


.rebounding-table{
  position: sticky;
  /* top: 2000px; */
  /* left: 700px; */
  width: 30vw;
  height: 56vh;
  margin: 5 10%;
  border-radius: 20px;
  background-color: black;
  overflow-y: scroll; 
  
}
.rebounding-table::-webkit-scrollbar{
  display: none;
}
.rebounding-table table{
  width: 100%;
  height: 100%;
}

.rebounding-table table thead {
  width: 100%;
  height: 60px;
  border-bottom: 1px solid #9F8950;
  font :bold 22px 'Bai Jamjuree';
  position:relative;
  background: color black;;
}

.rebounding-table table thead th {
  padding-left: 20px;
  position: sticky;
  background-color: black;
  top: 0px;
}

.rebounding-table table tbody {
  width: 100%;
  height: 480px;
  /* overflow-y: auto; */
}
.rebounding-table table tbody tr {
  width: 100%;
  height: 20%;
  text-align: center;
  border-bottom: 1px solid #9F8950;
}
.rebounding-table table tbody tr:last-child {
  border: none;
}
.rebounding-table table tbody td {
  font: bold 22px "Bai Jamjuree";
  width: 35%; 
}
.rebounding-table table tbody td:first-child {
  width: 2%;
}
.rebounding-table table tbody td:nth-child(2) {
  width: 3%;
}

.rebounding-table table tbody td:nth-child(n+3) {
  width: 3%;
}

.rebounding-table table tbody td p:first-child{
    color: white;
}

.rebounding-table table tbody td p:nth-child(2){
    color: #9F8950;
}

</style>