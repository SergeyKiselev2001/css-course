<template>

  <task-1 v-if="this.current_page==1"></task-1>
  <div 
    v-if="this.current_page!=1"
    class="space">
    В стадии разработки ;)
  </div>
  <div class="nav-panel">
    <div class="nav-panel__page"
        v-for="page in pages"
        :key="page"
        v-bind:class="{'nav-panel__page_active':this.current_page==page}"
        @click="pageChanging(page)"
    >{{page}}</div>
  </div>
</template>

<script>

 import Task1 from './Task1.vue';


export default {
  name: 'App',
  components: {
     Task1
  },

  data(){
    return {
      current_page : 1,
      pages : [1,2,3,4,5,6]
    }
  },

  methods: {
    pageChanging(page){
      this.current_page = page;
    }
  }
};
</script>
<style scoped>

.space{
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 30px;
  font-family: 'Montserrat', sans-serif;
}

.nav-panel {
  font-size: 18px;
  font-family: 'Montserrat', sans-serif;
  position: absolute;
  height: 70px;
  width: 400px;
  margin-top: -120px;
  margin-left: 50%;
  transform: translate(-50%, 0);
  border-radius: 40px;
  background-color: rgb(255, 255, 255);
  display: flex;
  justify-content: space-around;
  align-items: center;
  box-shadow: 0 0 10px black;
}

.nav-panel__page{
  height: 50px;
  width: 50px;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  box-shadow: 0 0 10px black;
}

.nav-panel__page:hover{
  background-color: rgb(73, 73, 73);
  cursor: pointer;
}

.nav-panel__page_active{
  background-color: rgb(148, 148, 148);
}

</style>
