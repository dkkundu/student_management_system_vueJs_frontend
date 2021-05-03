<template>
<div id ='app'>
  <NaVBar />
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
