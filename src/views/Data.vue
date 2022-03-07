<template>
  <div class="data">
    <div id="title">
      <h1>statistic</h1>
    </div>
    <Ranking />
    
    <div class="tables">
      <RankingTable />
      <div class = "item">
        <Score />
        <Rebound />
      </div>      
    </div>

  </div> 
</template>

<script>
import Ranking from '../components/ranking/Ranking.vue'
import RankingTable from '../components/ranking/RankingTable.vue'
import Score from '../components/ranking/Score.vue'
import Rebound from '../components/ranking/Rebound.vue'

export default {
  components: { Ranking, RankingTable, Score, Rebound },
  setup() {

  }
};
</script>

<style scoped>
.data{
  width: 100%;
  height: 200vh;
  background-color: #2f2f2f;
  color: white;
}

#title {
  position: fixed;
  top: 100px;
  width: 100%;
  height: 75px;
  background: linear-gradient( 269.04deg,rgba(159,137,80,0.495) 57.82%, rgba(89,81,61,0) 85.4%) ;
  text-transform: uppercase;
  padding-left: 5%;
  display: flex;
  align-items: flex-end;
  font:bold 0.6em 'Bai Jamjuree';
  letter-spacing: 0.6em;
}
.tables {
  position: fixed;
  width: 100%;
  top: 350px;
  height: 500px;
  overflow-y: scroll;
}

.tables::-webkit-scrollbar {
  display: none;
}

.item { 
  width: 80%;
  margin: 5%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}


</style>