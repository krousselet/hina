<template>
  <main class="flex-mobile">
    <div class="image-container appear-animation">
      <img
        src="../../public/images/desktop/home-background.png"
        alt="image de jardin japonais nuit"
        srcset=""
      />
    </div>
    <!-- <div class="background-dark appear-animation"> -->
      <div class="text-container appear-animation delay-1">
        <p>apprendre</p>
      </div>
      <div class="text-container appear-animation delay-2">
        <p>en</p>
      </div>
      <div class="text-container appear-animation delay-3">
        <p>s'amusant</p>
      </div>
    <!-- </div> -->
  </main>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped lang="scss">

// STRUCTURE

main {
    width: 100%;

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
      animation: appear 1s .5s ease-in-out forwards;
    }
    .text-container {
      overflow-x: hidden;
      position: relative;
      font-size: 2.5rem;
      text-transform: uppercase;
      animation: appear 1s ease-in-out forwards,
        move-from-right 1s 0.5s ease-in-out forwards;

      // Loop to apply incremental delays
      @for $i from 1 through 3 {
        &.delay-1 {
          animation-delay: 1s;
        }
        &.delay-2 {
          animation-delay: 1.5s;
        }
        &.delay-3 {
          animation-delay: 2s;
        }
      }
    }
  }

@media (min-width: 320px) and (max-width: 550px) {
  main {
    width: 100%;

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
      animation: appear 1s .5s ease-in-out forwards;
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
  .image-container {
      min-width: 991px;
      max-width: 1024px;
      height: 100%;
  }
}
</style>
