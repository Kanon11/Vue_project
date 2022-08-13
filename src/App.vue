<template>
  <div id="app">
  <!-- <log-in :kanon="xy"></log-in> -->
  <modal-view></modal-view>
  </div>
</template>

<script>


// import LogIn from './components/LogIn.vue';
import modalView from './components/modalView.vue';
export default {
  name: 'App',
  components: {
    // LogIn,
    modalView
  },
  data(){
    return{
      xy:20,
    }
  }
}
</script>


