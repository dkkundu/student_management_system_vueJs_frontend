<template>
<div id ='navbar'>
   <NaVBar />
</div>
<div id ='app'>
  <DataTable />
</div>
</template>

<script>
import DataTable from './components/DataTable.vue'
import NaVBar from './components/NavBar.vue'


export default {
  name: 'App',
  components: {
    DataTable,
    NaVBar,
  }
  
  }
  
</script>


<style>
</style>
