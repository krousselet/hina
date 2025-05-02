<template>
    <div class="home">
      <AlphabetComponent/>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import AlphabetComponent from '@/components/AlphabetComponent.vue'
  
  export default {
    name: 'AlphabetView',
    components: {
      AlphabetComponent
    }
  }
  </script>
  