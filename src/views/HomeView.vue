<template>
  <RevealComponent></RevealComponent>
    <HomeComponent/>
</template>

<script>
// @ is an alias to /src
import HomeComponent from '@/components/HomeComponent.vue'
import RevealComponent from '@/components/RevealComponent.vue';

export default {
  name: 'HomeView',
  components: {
    HomeComponent,
    RevealComponent
  }
}
</script>
