<template>
  <div id="alphabet-container">
    <div class="nihon-container">
      <img
        src="../../public/images/desktop/nihon.png"
        alt="image du drapeau du japon"
        srcset=""
      />
    </div>
    <div class="sakura-container-left no-scroll">
      <img
        src="../../public/images/desktop/sakura.png"
        alt="image de fleur de cerisier"
        srcset=""
      />
    </div>
    <div class="sakura-container-right no-scroll">
      <img
        src="../../public/images/desktop/sakura.png"
        alt="image de fleur de cerisier"
        srcset=""
      />
    </div>
    <div class="wrapper-left wrapper">
      <div class="container">
        <div class="title-container">
          <p>hiragana</p>
        </div>
        <div class="title-symbols-container">
          <p>ひらがな</p>
        </div>
      </div>
      <div class="chart">
        <table id="hiragana">
          <tr>
            <th></th>
            <th>a</th>
            <th>i</th>
            <th>u</th>
            <th>e</th>
            <th>o</th>
          </tr>
          <tr>
            <td></td>
            <td>あ</td>
            <td>い</td>
            <td>う</td>
            <td>え</td>
            <td>お</td>
          </tr>
          <tr>
            <td>k</td>
            <td>か</td>
            <td>き</td>
            <td>く</td>
            <td>け</td>
            <td>こ</td>
          </tr>
          <tr>
            <td>s</td>
            <td>さ</td>
            <td>し</td>
            <td>す</td>
            <td>せ</td>
            <td>そ</td>
          </tr>
          <tr>
            <td>t</td>
            <td>た</td>
            <td>ち</td>
            <td>つ</td>
            <td>て</td>
            <td>と</td>
          </tr>
          <tr>
            <td>n</td>
            <td>な</td>
            <td>に</td>
            <td>ぬ</td>
            <td>ね</td>
            <td>の</td>
          </tr>
          <tr>
            <td>h</td>
            <td>は</td>
            <td>ひ</td>
            <td>ふ</td>
            <td>へ</td>
            <td>ほ</td>
          </tr>
          <tr>
            <td>m</td>
            <td>ま</td>
            <td>み</td>
            <td>む</td>
            <td>め</td>
            <td>も</td>
          </tr>
          <tr>
            <td>y</td>
            <td>や</td>
            <td></td>
            <td>ゆ</td>
            <td></td>
            <td>よ</td>
          </tr>
          <tr>
            <td>r</td>
            <td>ら</td>
            <td>り</td>
            <td>る</td>
            <td>れ</td>
            <td>ろ</td>
          </tr>
          <tr>
            <td>w</td>
            <td>わ</td>
            <td></td>
            <td></td>
            <td></td>
            <td>を</td>
          </tr>
          <tr>
            <td>n</td>
            <td colspan="5">ん</td>
          </tr>
        </table>
      </div>
    </div>
    <div class="wrapper-right wrapper">
      <div class="title-container">
        <p>katakana</p>
      </div>
      <div class="title-symbols-container">
        <p>カタカナ</p>
      </div>
      <div class="chart">
        <table id="katakana">
          <tr>
            <th></th>
            <th>a</th>
            <th>i</th>
            <th>u</th>
            <th>e</th>
            <th>o</th>
          </tr>
          <tr>
            <td></td>
            <td>ア</td>
            <td>イ</td>
            <td>ウ</td>
            <td>エ</td>
            <td>オ</td>
          </tr>
          <tr>
            <td>k</td>
            <td>カ</td>
            <td>キ</td>
            <td>ク</td>
            <td>ケ</td>
            <td>コ</td>
          </tr>
          <tr>
            <td>s</td>
            <td>サ</td>
            <td>シ</td>
            <td>ス</td>
            <td>セ</td>
            <td>ソ</td>
          </tr>
          <tr>
            <td>t</td>
            <td>タ</td>
            <td>チ</td>
            <td>ツ</td>
            <td>テ</td>
            <td>ト</td>
          </tr>
          <tr>
            <td>n</td>
            <td>ナ</td>
            <td>ニ</td>
            <td>ヌ</td>
            <td>ネ</td>
            <td>ノ</td>
          </tr>
          <tr>
            <td>h</td>
            <td>ハ</td>
            <td>ヒ</td>
            <td>フ</td>
            <td>ヘ</td>
            <td>ホ</td>
          </tr>
          <tr>
            <td>m</td>
            <td>マ</td>
            <td>ミ</td>
            <td>ム</td>
            <td>メ</td>
            <td>モ</td>
          </tr>
          <tr>
            <td>y</td>
            <td>ヤ</td>
            <td></td>
            <td>ユ</td>
            <td></td>
            <td>ヨ</td>
          </tr>
          <tr>
            <td>r</td>
            <td>ラ</td>
            <td>リ</td>
            <td>ル</td>
            <td>レ</td>
            <td>ロ</td>
          </tr>
          <tr>
            <td>w</td>
            <td>ワ</td>
            <td></td>
            <td></td>
            <td></td>
            <td>ヲ</td>
          </tr>
          <tr>
            <td>n</td>
            <td colspan="5">ン</td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlphabetComponent",

  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">
$background-black: rgba(0, 0, 0, 0.945);

@media (min-width: 320px) and (max-width: 991px) {
  #alphabet-container {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    outline: 1px solid black;
    position: relative;

    .nihon-container {
      position: absolute;
      left: 50%;
      top: 50px;
      transform: translateX(-50%);
    }

    .sakura-container-left {
      position: absolute;
      left: -4%;
      top: 50px;
    }

    .sakura-container-right {
      position: absolute;
      right: 4%;
      top: 50px;
    }
    .wrapper {
      outline: 1px solid rgba(255, 0, 0, 0.155);
      background-color: $background-black;
      .container {
        margin-top: 160px;
      }
      .title-container {
        font-size: 5vw;
      }
      .title-symbols-container {
        font-size: 5vw;
      }

      .chart {
        display: grid;
        font-size: 5vw;
      }
    }
  }
  img {
    width: 50%;
    height: 50%;
  }
}

//FONTS
th,
td,
p {
  color: white;
}

@media (min-width: 992px) {
  #alphabet-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    outline: 1px solid rgb(0, 0, 0);
    position: relative;

    .nihon-container {
      position: absolute;
      left: 50%;
      top: 5%;
      transform: translateX(-50%);
    }

    .sakura-container-left {
      position: absolute;
      left: 0%;
      top: 50px;

      img {
        animation: rotation-left 13s 0.2s infinite;
      }
    }

    .sakura-container-right {
      position: absolute;
      right: 0%;
      top: 50px;
      img {
        animation: rotation-right 13s 0.2s infinite;
      }
    }

    .wrapper {
      outline: 1px solid rgba(255, 0, 0, 0.155);
      background-color: $background-black;
      .title-container {
        font-size: 3rem;
      }
      .title-symbols-container {
        font-size: 3rem;
      }

      .chart {
        display: grid;
        font-size: 3rem;
        .row {
        }
      }
    }
  }
}

.wrapper {
}

@keyframes rotation-right {
  0% {
    transform: rotate(0);
  }

  50% {
    transform: rotate(180deg) scale(0.5);
  }

  100% {
    transform: rotate(0);
  }
}

@keyframes rotation-left {
  0% {
    transform: rotate(0);
  }

  50% {
    transform: rotate(-180deg) scale(0.5);
  }

  100% {
    transform: rotate(0);
  }
}
</style>
