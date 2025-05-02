<template>
      <DrawComponent v-if="isDrawComponentVisible"/>
  </template>
  
  <script>
  // @ is an alias to /src
  import DrawComponent from '@/components/DrawComponent.vue'
  
  export default {
    name: 'DrawComponent',
    components: {
      DrawComponent
    }
  }
  </script>
  