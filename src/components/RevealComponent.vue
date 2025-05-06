<template>
    <h2 class="block-effect" style="--td: 1.2s">
    <div class="block-reveal" style="--bc: yellow; --d: .1s">{{ textOne }}</div>
    <div class="block-reveal" style="--bc:  rgba(255, 220, 0, 1); --d: .5s">{{textTwo}}</div>
    </h2>
  </template>
  rgba(175, 175, 33, 0.774), yellow
  <script>
  export default {
    name: 'RevealComponent',
    data() {
      return {
        textOne: "Nihongo",
        textTwo: "Ensemble"
      }
    }
  }
  </script>
  
  <style scoped lang="scss">

p {
  color: #2e2e2e;
  margin-bottom: 20px;
}


/* block-$ */
.block-effect {
  font-size: calc(8px + 6vw);
}

.block-reveal {
  background-color: white;
  --t: calc(var(--td) + var(--d));

  color: transparent;
  padding: 4px;

  position: relative;
  overflow: hidden;
  border-radius: 0px;

  animation: revealBlock 0s var(--t) forwards;
}

.block-reveal::after {
  content: '';

  width: 0%;
  height: 100%;
  padding-bottom: 4px;
  border-radius: 0;

  position: absolute;
  top: 0;
  left: 0;

  background: var(--bc);
  animation: revealingIn var(--td) var(--d) forwards, revealingOut var(--td) var(--t) forwards;
}


/* animations */
@keyframes revealBlock {
  100% {
    color: black;
  }
}

@keyframes revealingIn {

  0% {
    width: 0;
  }

  100% {
    width: 100%;
  }
}

@keyframes revealingOut {

  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(100%);
  }

}

  </style>