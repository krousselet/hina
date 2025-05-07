<template>
  <nav>
    <router-link class="underline-hover-effect" to="/">Home</router-link> |
    <router-link class="underline-hover-effect" to="/draw">Dessiner</router-link> |
    <router-link class="underline-hover-effect" to="/alphabet">Alphabet</router-link>
  </nav>
  <router-view/>
</template>

<style lang="scss">

// IMPORTS

@import url('https://fonts.googleapis.com/css2?family=Caveat+Brush&display=swap');

//SCROLLBAR CUSTOMIZATION


//FIREFOX

* {
  scrollbar-width: thin;           /* auto | thin | none */
  scrollbar-color: #C70025 #f0f0f0;   /* thumb track */
}

// GENERAL CLASSES

// GLOBAL ANIMATIONS — Consider moving to a global SCSS file or `_animations.scss` partial
@keyframes draw {
  0% {
    stroke-dashoffset: 1000;
    stroke-opacity: 0;
  }
  1% {
    stroke-opacity: 1;
  }
  100% {
    stroke-dashoffset: 0;
  }
}

.no-scroll {
  overflow: hidden;
}

.underline-hover-effect {
  background: none;
  outline: none;
  border: none;
  display: inline-flex;
  position: relative;   
  cursor: pointer;      
  justify-content: center;
  align-items: center;
}

.underline-hover-effect::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0;
  height: 2px;
  background: black;
  transition: width 0.2s ease;
  transform: translateX(-50%);
}

.underline-hover-effect:hover::after {
  width: 100%;
  transition: width 0.2s ease;
}

.text-mobile {
  font-size: 1rem;
}

.text-tablet {
  font-size: 1.3rem;
}

.text-desktop {
  font-size: 1.7rem;
}

.h2 {
  font-size: 3rem;
}

.appear-animation {
  opacity: 0;
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}

.flex-mobile {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.gradient {
  background: #ddd6f3;
  background: linear-gradient(to top, grey, rgba(175, 175, 33, 0.774), yellow);
}

.background-dark {
  background-color: black;
  color: white;
  width: 100%;
}

.background-light {
  background-color: white;
  color: black;
}

// VARIABLES

// FONTS

.caveat-brush-regular {
  font-display: swap;
  font-family: "Caveat Brush", cursive;
  font-weight: 400;
  font-style: normal;
}

//STRUCTURE

body {
  margin: 0 !important;
  padding: 0 !important;
  box-sizing: border-box !important;
  
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-family: "Caveat Brush", cursive;
}

nav {
  padding: 30px;
  display: flex;
  justify-content: space-around;
  align-items: center;

  a {
    font-weight: bold;
    color: black;
    font-size: 3vw;
    text-decoration: none;

    &.router-link-exact-active {
      color: #C70025;
    }
  }
}

// ANIMATIONS

// SVG AUTO DRAWING

@keyframes draw {
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes appear {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

@keyframes move-from-left {
  0% {
    left: -25vw;
  }
  100% {
    left: 0;
  }
}

@keyframes move-from-right {
  0% {
    right: -25vw;
  }
  100% {
    right: 0;
  }
}
</style>
