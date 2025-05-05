<template>
  <main>
    <div class="title-container">
      <h2 class="h2">Dessiner Hiragana / Katakana</h2>
    </div>
    <!-- Kana Selection -->
    <div class="controls">
      <select v-model="kanaType" class="text-desktop">
        <div class="container">
          <option value="hiragana">Hiragana</option>
          <img src="../../public/models/hiragana/a.svg" />
        </div>
        <div class="container">
          <option value="katakana">Katakana</option>
          <img src="../../public/models/katakana/a.svg" />
        </div>
      </select>

      <select v-model="selectedKana" class="text-desktop">
        <option v-for="kana in kanaList" :key="kana" :value="kana">
          {{ kana }}
        </option>
      </select>

      <button class="underline-hover-effect" @click="clearCanvas">Effacer</button>
      <button class="underline-hover-effect" @click="scoreDrawing">Valider</button>
    </div>

    <!-- Canvas and model overlay -->
    <div class="canvas-wrapper">
      <img :src="modelImagePath" class="kana-model" />
      <canvas ref="drawCanvas" width="400" height="400" />
    </div>

    <transition name="fade-score">
  <div class="score" v-if="score !== null">Score: {{ score }}%</div>
</transition>
  </main>
</template>

<script>
import confetti from "canvas-confetti";
export default {
  name: "DrawComponent",

  data() {
    return {
      drawing: false,
      canvas: null,
      ctx: null,
      kanaType: "hiragana",
      selectedKana: "a",
      score: null,
      kanaList: [
        "a",
        "i",
        "u",
        "e",
        "o",
        "ka",
        "ki",
        "ku",
        "ke",
        "ko",
        "sa",
        "shi",
        "su",
        "se",
        "so",
        "ta",
        "chi",
        "tsu",
        "te",
        "to",
        "na",
        "ni",
        "nu",
        "ne",
        "no",
        "ha",
        "hi",
        "fu",
        "he",
        "ho",
        "ma",
        "mi",
        "mu",
        "me",
        "mo",
        "ya",
        "yu",
        "yo",
        "ra",
        "ri",
        "ru",
        "re",
        "ro",
        "wa",
        "wo",
        "n",
      ],
    };
  },

  computed: {
    modelImagePath() {
      return `/models/${this.kanaType}/${this.selectedKana}.svg`; // Image path
    },
  },

  mounted() {
    this.canvas = this.$refs.drawCanvas;
    this.ctx = this.canvas.getContext("2d");

    // Mouse Events
    this.canvas.addEventListener("mousedown", this.startDraw);
    this.canvas.addEventListener("mousemove", this.draw);
    this.canvas.addEventListener("mouseup", this.endDraw);
    this.canvas.addEventListener("mouseout", this.endDraw);

    // Touch Events
    this.canvas.addEventListener("touchstart", this.startDraw, {
      passive: false,
    });
    this.canvas.addEventListener("touchmove", this.draw, { passive: false });
    this.canvas.addEventListener("touchend", this.endDraw);
  },

  methods: {
    getPos(e) {
      const rect = this.canvas.getBoundingClientRect();
      if (e.touches) {
        return {
          x: e.touches[0].clientX - rect.left,
          y: e.touches[0].clientY - rect.top,
        };
      } else {
        return {
          x: e.clientX - rect.left,
          y: e.clientY - rect.top,
        };
      }
    },

    startDraw(e) {
      e.preventDefault();
      this.drawing = true;
      const pos = this.getPos(e);
      this.ctx.beginPath();
      this.ctx.moveTo(pos.x, pos.y);
    },

    draw(e) {
      if (!this.drawing) return;
      e.preventDefault();
      const pos = this.getPos(e);
      this.ctx.lineTo(pos.x, pos.y);
      this.ctx.strokeStyle = "black";
      this.ctx.lineWidth = 35;
      this.ctx.lineCap = "round";
      this.ctx.stroke();
    },

    endDraw(e) {
      e.preventDefault();
      this.drawing = false;
      this.ctx.beginPath();
    },

    clearCanvas() {
      this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
      this.score = null;
    },

    scoreDrawing() {
      const userData = this.ctx.getImageData(0, 0, 400, 400).data;

      const modelImg = new Image();
      modelImg.crossOrigin = "Anonymous";
      modelImg.src = this.modelImagePath;

      modelImg.onload = () => {
        const tempCanvas = document.createElement("canvas");
        tempCanvas.width = 400;
        tempCanvas.height = 400;
        const tempCtx = tempCanvas.getContext("2d");

        tempCtx.fillStyle = "white";
        tempCtx.fillRect(0, 0, 400, 400);

        tempCtx.drawImage(modelImg, 0, 0, 400, 400);
        const modelData = tempCtx.getImageData(0, 0, 400, 400).data;

        let match = 0,
          modelInk = 0;

        for (let i = 0; i < modelData.length; i += 4) {
          const modelAlpha = modelData[i + 3];
          const modelBlack = modelData[i] < 100 && modelAlpha > 50;

          if (modelBlack) {
            modelInk++;

            const userAlpha = userData[i + 3];
            const userBlack = userData[i] < 100 && userAlpha > 50;

            if (userBlack) match++;
          }
        }

        const scoreValue = modelInk ? Math.round((match / modelInk) * 100) : 0;
        this.score = scoreValue;

        if (scoreValue >= 80) {
          confetti({
            particleCount: 100,
            spread: 70,
            origin: { y: 0.6 },
          });
        }
      };
    },
  },
};
</script>

<style scoped lang="scss">

// TRANSITION EFFECT

.fade-score-enter-active,
.fade-score-leave-active {
  transition: opacity 0.5s ease, transform 0.5s ease;
}
.fade-score-enter-from,
.fade-score-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
.fade-score-enter-to,
.fade-score-leave-from {
  opacity: 1;
  transform: translateY(0);
}
main {
  display: grid;

  .controls {
    margin: 10px;
    display: flex;
    gap: 10px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .container {
      display: flex;
      img {
        width: 25px;
        height: 25px;
      }
    }

    select,
    select::picker(select) {
      appearance: base-select;
      border-radius: 7px;
    }
  }
  .canvas-wrapper {
    position: relative;
    width: 400px;
    height: 400px;
    margin: 10px auto;

    .kana-model {
      position: absolute;
      top: 0;
      left: 0;
      width: 400px;
      height: 400px;
      opacity: 0.3;
      pointer-events: none;
      // z-index: 2;
    }

    canvas {
      position: absolute;
      top: 0;
      left: 0;
      border: 2px solid #333;
      touch-action: none;
      background-color: rgba(0, 0, 0, 0.05);
      border-radius: 7px;
    }
  }
  .score {
    margin-top: 10px;
    font-size: 1.2em;
    font-weight: bold;
  }
}

@media (min-width: 991px) {
  main {
    width: 75%;
    height: 100%;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-template-areas:
      "top top top"
      "left middle right";
      margin: 0 auto;

    .title-container {
      grid-area: top;
      width: 100%;
    }

    .canvas-wrapper {
      grid-area: left;
    }
    .controls {
     grid-area: middle;
    }

    .score {
      grid-area: right;
      font-size: 2rem;
      margin: 10px;
      display: flex;
      gap: 10px;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
    }

  }

}
</style>
