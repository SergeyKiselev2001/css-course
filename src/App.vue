<template>

  <task-1 
    class='abs'
    :class="{'animation-in':this.picked_page == 1,
             'animation-out':this.picked_page != 1}"
    v-if="this.current_page==1 || this.picked_page == 1"
  />

  <task-2 
    class='abs'
    :class="{'animation-in':this.picked_page == 2,
             'animation-out':this.picked_page != 2}"
    v-if="this.current_page==2 || this.picked_page == 2"
  />
  
  <task-3 
    class='abs'
    :class="{'animation-in':this.picked_page == 3,
             'animation-out':this.picked_page != 3}"
    v-if="this.current_page==3 || this.picked_page == 3"
  />

  <task-4 
    class='abs'
    :class="{'animation-in':this.picked_page == 4,
             'animation-out':this.picked_page != 4}"
    v-if="this.current_page==4 || this.picked_page == 4"
  />

  <task-5 
    class='abs'
    :class="{'animation-in':this.picked_page == 5,
             'animation-out':this.picked_page != 5}"
    v-if="this.current_page==5 || this.picked_page == 5"
  />

  <task-6 
    class='abs'
    :class="{'animation-in':this.picked_page == 6,
             'animation-out':this.picked_page != 6}"
    v-if="this.current_page==6 || this.picked_page == 6"
  />
  
  
  <!-- <div 
    v-if="this.current_page>2"
    class="space">
    В стадии разработки ;)
  </div> -->
  <div class="nav-panel">
    <div class="nav-panel__page"
        v-for="page in pages"
        :key="page"
        v-bind:class="{'nav-panel__page_active':this.picked_page==page}"
        @click="pageChanging(page)"
    >{{page}}</div>
  </div>
</template>

<script>

import Task1 from './Task1.vue';
import Task2 from './Task2.vue';
import Task3 from './Task3.vue';
import Task4 from './Task4.vue';
import Task5 from './Task5.vue';
import Task6 from './Task6.vue';


export default {
  name: 'App',
  components: {
     Task1,
     Task2,
     Task3,
     Task4,
     Task5,
     Task6,

  },

  data(){
    return {
      current_page : 1,
      pages : [1,2,3,4,5,6],

      is_page_changed: false,

      picked_page: 1,
    }
  },

  watch:{
    current_page(){
      this.is_page_changed = true;
    },
  },

  methods: {
    pageChanging(page){
      this.picked_page = page;


      setTimeout(()=>{this.current_page = page;}, 701);
    }
  }
};
</script>
<style>


#app{
  overflow: hidden;
}

.animation-in{
  z-index: 10;
  overflow: hidden;
  animation: top-to-center .7s linear 0s 1 forwards;
}

.animation-out{
  z-index: 9;
  overflow: hidden;
  animation: center-to-bottom 1.1s linear .1s 1 forwards;
}


@keyframes top-to-center {
    0%{
        transform: translate(0%, -200%);
    }

    100%{
        transform: translate(0%, 0%);
    }
}

@keyframes center-to-bottom {
    0%{
        transform: translate(0%, 0%);
    }

    100%{
        transform: translate(0%, 100%);
    }
}

.abs{
  overflow: hidden;
  position: absolute;
}

.space{
  z-index: 4;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 30px;
  color: white;
  font-family: 'Montserrat', sans-serif;
}

.nav-panel {
  z-index: 100;
  font-size: 18px;
  font-family: 'Montserrat', sans-serif;
  position: absolute;
  height: 70px;
  width: 400px;
  margin-top: 920px;
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
