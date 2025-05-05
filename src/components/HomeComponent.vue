<template>
  <main class="flex-mobile">
    <div class="image-container appear-animation">
      <picture>
        <source
          srcset="../../public/images/mobile/home-background.webp"
          media="(max-width: 600px)"
          type="image/webp"
        />
        <!-- WebP fallback for desktop -->
        <source
          srcset="../../public/images/desktop/home-background.webp"
          type="image/webp"
        />
        <!-- Fallback PNG -->
        <img
          src="../../public/images/desktop/home-background.png"
          alt="image de jardin japonais nuit"
          width="1920"
          height="1080"
          loading="eager"
          decoding="async"
          fetchpriority="high"
          style="width: 100%; height: auto; display: block;"
        />
      </picture>
    </div>
    <!-- <div class="background-dark appear-animation"> -->
      <div class="container">
        <div class="text-container appear-animation delay-1">
          <p>apprendre</p>
        </div>
        <div class="text-container appear-animation delay-2">
          <p>en</p>
        </div>
        <div class="text-container appear-animation delay-3">
          <p>s'amusant</p>
        </div>
      </div>
      <div class="container">
        <div class="text-container appear-animation delay-4">
          <p>test</p>
        </div>
        <div class="text-container appear-animation delay-5">
          <p>test</p>
        </div>
        <div class="text-container appear-animation delay-6">
          <p>test</p>
        </div>
      </div>
    <!-- </div> -->
  </main>

  <!-- AUTOMATICALLY DRAW LETTERS IN THE BROWSER -->
  <svg width="75" height="75" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M 24.8632 1 C 24.788 12.2465 24.8651 20.6457 25.3326 28.4655 M 29 60 C 27.7726 52.2462 25.7534 35.5044 25.3326 28.4655 M 9.63766 12.1897 C 31.3012 12.8413 44.7012 13.6744 52.4597 9.13793 M 41.9921 22.3621 C 35.5479 43.3409 23.2329 65 9.63766 54.9138 C -3.95762 44.8276 9.31421 36.4502 25.3326 28.4655 M 25.3326 28.4655 C 41.5438 25.414 48.6714 26.6572 56.2661 36.6034 C 58.1555 49.3134 59.6706 56.6074 36.2825 60"
    stroke="black"
    stroke-width="3"
    fill="none"
    stroke-dasharray="1000"
    stroke-dashoffset="1000"
    style="filter: drop-shadow(0 0 2px rgba(0,0,0,0.3));"
  />
</svg>








</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped lang="scss">
// STRUCTURE

path {
  animation: draw 14s ease-in-out forwards;
}

@keyframes draw {
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes fadeIn {
  0% {
    stroke-opacity: 0;
  }
  50% {
    stroke-opacity: 0.5;
  }
  100% {
    stroke-opacity: 1;
  }
}

@keyframes pulseWidth {
  0%, 100% {
    stroke-width: 6.2;
  }
  50% {
    stroke-width: 7.5; /* Slight pressure illusion */
  }
}

main {
  width: 100%;

  .image-container {
    width: 100%;
    height: 100%;
    animation: appear 1s 0.5s forwards ease-in-out;
    

    img {
      width: 100%;
      height: 100%;
      border-radius: 7px;
    }
  }
  // MOVE THIS IN THE APP SO IT IS USABLE GLOBALLY

  .background-dark {
    margin-top: 20px;
    animation: appear 1s 0.5s ease-in-out forwards;
  }
  .text-container {
    overflow-x: hidden;
    position: relative;
    font-size: 2.5rem;
    text-transform: uppercase;
    animation: appear 1s ease-in-out forwards,
      move-from-right 1s 0.5s ease-in-out forwards;

    // Loop to apply incremental delays
    @for $i from 1 through 6 {
      &.delay-1 {
        animation-delay: 1s;
      }
      &.delay-2 {
        animation-delay: 1.5s;
      }
      &.delay-3 {
        animation-delay: 2s;
      }
      &.delay-4 {
        animation-delay: 2.5s;
      }
      &.delay-5 {
        animation-delay: 3s;
      }
      &.delay-6 {
        animation-delay: 3.5s;
      }
    }
  }
}

@media (min-width: 320px) and (max-width: 550px) {
  main {

    .image-container {
      width: 100%;
      height: 100%;
      animation: appear 1s 0.5s forwards ease-in-out;

      img {
        width: 100%;
        height: 100%;
      }
    }
    // MOVE THIS IN THE APP SO IT IS USABLE GLOBALLY

    .background-dark {
      margin-top: 20px;
      animation: appear 1s 0.5s ease-in-out forwards;
    }
  }
}

@media (min-width: 551px) and (max-width: 991px) {
  .image-container {
    min-width: 551px;
    max-width: 991px;
    height: 100%;
  }
}

@media (min-width: 991px) and (max-width: 4080px) {
  main {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-template-areas: "left middle right";
    width: 100%;
    height: 100%;
    overflow: hidden;
    margin: 0 auto;
    margin-bottom: 15px;

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      
    }

    .container:nth-child(1) {
      grid-area: left;
      width: 100%;
      height: 100%;
    }
    .image-container {
      width: 100%;
      height: 100%;
      grid-area: middle;
    }
  
    .container:nth-child(2) {
        grid-area: right;
        width: 100%;
        height: 100%;
      }
  }
}
</style>
