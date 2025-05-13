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
          style="width: 100%; height: auto; display: block"
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
      <div class="image-container visible">
        <!-- ta -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="57"
          height="61"
          viewBox="0 0 57 61"
          fill="none"
          stroke="black"
          stroke-width="3"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
          stroke-linecap="round"
        >
          <path
            class="letter-path"
            d="M1 15.8074C17.9934 16.0183 26.55 15.55 37 11.8074M18 0.807373C14.4146 25.6844 12.1979 39.4296 3 58.8074M32 25.8074L56 24.8074M32 39.8074C28.1619 50.1071 27.155 55.1064 36 56.8074H56"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- no -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="61"
          height="55"
          viewBox="0 0 61 55"
          fill="none"
          stroke-width="3"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M33.1389 4.04891C27.5805 34.0919 24.2891 48.389 11.2888 47.389C-1.71142 46.389 0.288988 6.38911 21.2888 4.38906C42.2886 2.389 64.2886 6.38904 56.2887 38.389C52.4086 49.4907 47.1582 52.5658 31.2888 51.389"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- shi -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="49"
          height="58"
          viewBox="0 0 49 58"
          fill="none"
          stroke-width="3"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M5.22222 1.18701C5.22222 1.18701 0.222222 34.187 5.22222 46.187C10.2222 58.187 28.6913 57.5472 46.2222 41.187"
            stroke="black"
            stroke-width="6"
          />
        </svg>
      </div>
      <div class="image-container visible">
        <!-- ku -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="37"
          height="65"
          viewBox="0 0 37 65"
          fill="none"
          stroke-width="3"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M31 3.30737C31 3.30737 3 26.3074 3 30.3074C3 34.3074 35 62.3074 35 62.3074"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- be -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="64"
          height="47"
          viewBox="0 0 64 47"
          fill="none"
          stroke-width="3"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M2 32.5C2 32.5 25.5311 15.4839 29 16.5C32.4689 17.5161 50.6887 40.2777 63 43.5M41 9.5L49.5 20M49.5 2.5L57 12.5"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- n -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="63"
          height="62"
          viewBox="0 0 63 62"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M23.1285 1.80737C23.1285 1.80737 1.12854 49.8074 3.12854 55.8074C5.12854 61.8074 31.1287 12.8074 30.1287 35.8074C29.1287 58.8074 38.1287 59.8074 48.1287 57.8074C58.1287 55.8074 59.1287 35.8074 59.1287 35.8074"
            stroke="black"
            stroke-width="6"
          />
        </svg>
      </div>
      <div class="image-container visible">
        <!-- ki -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="54"
          height="62"
          viewBox="0 0 54 62"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M5 12.8628C22.6058 14.6912 31.616 13.6813 46 7.86279M1 26.8628C29.5607 27.4251 42.0078 26.7039 52 21.8628M25 0.862793C24.3466 21.9806 43 36.8628 43 39.8628C43 42.8628 28 35.8628 28 35.8628M16 39.8628C8.42102 46.8926 11 55.8628 16 57.8628C21 59.8628 43 57.8628 43 57.8628"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- yo -->
        <svg
          id="yo"
          xmlns="http://www.w3.org/2000/svg"
          width="54"
          height="41"
          viewBox="0 0 54 62"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M25.7513 0.501465C25.7513 0.501465 26.039 6.97447 26.287 15.5015M51.7514 52.5015C44.0575 46.0075 18.6118 32.2122 6.75144 40.5015C-7.24855 54.5015 23.7513 63.5015 25.7513 54.5015C26.9928 48.9149 26.693 29.4572 26.287 15.5015M26.287 15.5015L50.7515 14.5015"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- u -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="46"
          height="66"
          viewBox="0 0 46 66"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M1.57471 28.6533C44.2099 17.7632 61.5576 41.0638 13.985 62.7815M7.77984 3.83301L35.7029 9.00395"
            stroke="black"
            stroke-width="6.20513"
          />
        </svg>
      </div>
      <div class="image-container visible">
        <!-- su -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="61"
          height="66"
          viewBox="0 0 61 66"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M0.222168 14.8074L60.2222 12.8074M35.2222 0.807373C35.2222 0.807373 35.9573 13.6716 36.3133 25.8074M36.3133 25.8074C36.5446 33.6891 36.6159 41.2637 36.2222 44.8074C35.2222 53.8074 10.2222 45.8074 16.2222 33.8074C22.2222 21.8074 36.3133 25.8074 36.3133 25.8074ZM36.3133 25.8074C37.1141 45.7729 38.2222 58.8074 18.2222 62.8074"
            stroke="black"
            stroke-width="6"
          />
        </svg>
        <!-- ru -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="56"
          height="61"
          viewBox="0 0 56 61"
          fill="none"
          stroke-dasharray="1000"
          stroke-dashoffset="1000"
          style="filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.3))"
        >
          <path
            class="letter-path"
            d="M7.78271 6.46631L41.7827 4.46631C41.7827 4.46631 5.78271 37.4663 3.78271 40.4663C1.78271 43.4663 24.7829 24.4663 41.7827 26.4663C57.1596 28.2754 56.1726 50.5389 41.7827 55.5134M41.7827 55.5134C40.2639 56.0384 38.5959 56.3708 36.782 56.4663C18.0661 60.0235 9.78198 50.4663 20.782 44.4663C31.782 38.4663 41.7827 55.5134 41.7827 55.5134Z"
            stroke="black"
            stroke-width="6"
          />
        </svg>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped lang="scss">
// VARIABLES
$image-count: 11;
$delay-step: 0.8s;

// STRUCTURE

.visible {
  opacity: 1 !important;
}

main {
  width: 100%;

  .image-container {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
    height: 100%;
    animation: appear 1s 0.5s forwards ease-in-out;
    align-items: baseline;

    img {
      width: 100%;
      height: 100%;
      border-radius: 7px;
    }

    // Loop for staggered SVG letter animations
    @for $i from 1 through $image-count {
      svg:nth-of-type(#{$i}) .letter-path {
        animation: draw 10s ease-in-out forwards;
        animation-delay: ($i - 1) * $delay-step;
      }
    }
  }

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

    // Incremental text delays
    @for $i from 1 through 6 {
      &.delay-#{$i} {
        animation-delay: 0.5s + ($i * 0.5s);
      }
    }
  }
}

// MOBILE
@media (min-width: 320px) and (max-width: 550px) {
  main {
    .container {
      margin: 25px auto;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      align-items: center;
    }
    .image-container {
      width: 100%;
      height: 100%;
      animation: appear 1s 0.5s forwards ease-in-out;

      img {
        width: 100%;
        height: 100%;
      }
      svg {
        margin: 15px;
      }
    }

    .background-dark {
      margin-top: 20px;
      animation: appear 1s 0.5s ease-in-out forwards;
    }
  }
}

// TABLET
@media (min-width: 551px) and (max-width: 991px) {
  .image-container {
    min-width: 551px;
    max-width: 991px;
    height: 100%;
  }
}

// DESKTOP
@media (min-width: 991px) and (max-width: 4080px) {
  main {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr;
    grid-template-areas: "left middle right";
    width: 100%;
    height: 100%;
    overflow: hidden;
    margin: 0 auto 15px;

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
