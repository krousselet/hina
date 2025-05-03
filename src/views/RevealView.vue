<template>
    <RevealComponent :textOne="textOne" :textTwo="textTwo"></RevealComponent>
  </template>
  
  <script>
  // @ is an alias to /src
  import RevealComponent from '@/components/RevealComponent.vue';
  
  export default {
    name: 'HomeView',
    components: {
      RevealComponent
    },
    props: {
      textOne: String,
      textTwo: String,
    }
  }
  </script>
  