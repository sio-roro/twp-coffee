<template>
  <div class="hello">
    <header id="header">
      <div class="header-left">
        <a href="#top">Top</a>
      </div>
      <div class="header-right">
        <a href="#bland">Bland</a>
        <a href="#plan">Plan</a>
        <a href="#featured">Feature</a>
        <a href="#contact">Contact</a>
      </div>
    </header>
    <!--ハンバーガーメニューのボタン-->
    <div class="hamburger_btn" v-on:click="ActiveBtn = !ActiveBtn">
      <span
        class="line line_01"
        v-bind:class="{ btn_line01: ActiveBtn }"
      ></span>
      <span
        class="line line_02"
        v-bind:class="{ btn_line02: ActiveBtn }"
      ></span>
      <span
        class="line line_03"
        v-bind:class="{ btn_line03: ActiveBtn }"
      ></span>
    </div>
    <!--サイドバー-->
    <transition name="menu">
      <div class="menu" v-show="ActiveBtn">
        <ul>
          <li>
            <a href="#top" v-on:click="ActiveBtn = !ActiveBtn">Top</a>
          </li>
          <li>
            <a href="#bland" v-on:click="ActiveBtn = !ActiveBtn">Bland</a>
          </li>
          <li>
            <a href="#plan" v-on:click="ActiveBtn = !ActiveBtn">Plan</a>
          </li>
          <li>
            <a href="#featured" v-on:click="ActiveBtn = !ActiveBtn">Featured</a>
          </li>
          <li>
            <a href="#contact" v-on:click="ActiveBtn = !ActiveBtn">Contact</a>
          </li>
        </ul>
      </div>
    </transition>
    <div class="top1" id="top" v-scroll-reveal.reset="animation">
      <h1>何気ない日常に<br />健康の一杯を</h1>
    </div>
    <div class="top2" id="bland" v-scroll-reveal.reset="animation">
      <div class="top2-text">
        <h1 class="top2-head">Our Coffee Bland</h1>
        <p>
          プロ焙煎師が10カ国50銘柄以上から、高品質・有機やオーガニック・JAS認証などの複数の基準を用いて厳選した3種類の生豆を提供しています。
        </p>
        <p><i class="fas fa-coffee"></i></p>
      </div>
      <div class="top2-pic">
        <p><i class="fas fa-water water"></i></p>
        <i class="fas fa-arrow-down"></i>
        <div class="three-coffee">
          <div class="coffee-pac"><p class="soon">Comming soon</p></div>
          <h2 class="big">COLOMBIA</h2>
          <p class="kind">EXCELSO</p>
        </div>
        <p><i class="fas fa-water water"></i></p>
        <i class="fas fa-arrow-down"></i>
        <div class="three-coffee">
          <div class="coffee-pac"><p class="soon">Comming soon</p></div>
          <h2>ETHIOPIA</h2>
          <p class="kind">YIRGACHFFE</p>
        </div>
        <p><i class="fas fa-water water"></i></p>
        <i class="fas fa-arrow-down"></i>
        <div class="three-coffee">
          <div class="coffee-pac"><p class="soon">Comming soon</p></div>
          <h2>RAZIL</h2>
          <p class="kind">BOURBON</p>
        </div>
        <p><i class="fas fa-water"></i></p>
      </div>
    </div>
    <div class="top3" id="box" v-scroll-reveal.reset="animation">
      <h1>TWP Coffee</h1>
    </div>
    <div class="top4" id="box"></div>
    <div class="top5" id="box" v-scroll-reveal.reset="animation">
      <div class="top5-left">
        <h1>Coffee <br />Roasting</h1>
        <p>
          プロの焙煎師が毎週御社を訪問し、特別な焙煎機を用いて<span><br /></span
          >生豆からお好みの焙煎度合に応じて焙煎を行います。
        </p>
      </div>
      <div class="top5-right"></div>
    </div>
    <div class="top6" id="box" v-scroll-reveal.reset="animation">
      <div class="top6-right-flex">
        <h1>Coffee <br />at the Office</h1>
        <p>
          プロの焙煎師が毎週新たに生豆から焙煎を行うため、常に新鮮な焙煎豆を使用した健康に良いコーヒーを会社で飲むことができます。
        </p>
      </div>
      <div class="top6-left"></div>
      <div class="top6-right-nomal">
        <h1>Coffee <br />at the Office</h1>
        <p>
          プロの焙煎師が毎週新たに生豆から焙煎を行うため、常に<br />新鮮な焙煎豆を使用した健康に良いコーヒーを会社で飲<br />むことができます。
        </p>
      </div>
    </div>
    <div class="top7" id="plan" v-scroll-reveal.reset="animation">
      <div class="top7-conntent">
        <div class="price">
          <div class="price-image1"></div>
          <div class="price-text">
            <h3>¥35,000/月</h3>
            <p>10〜50人<br />200杯/月</p>
          </div>
        </div>
        <div class="price">
          <div class="price-image2"></div>
          <div class="price-text">
            <h3>¥45,000/月</h3>
            <p>50〜100人<br />300杯/月</p>
          </div>
        </div>
        <div class="price">
          <div class="price-image3"></div>
          <div class="price-text">
            <h3>¥55,000/月</h3>
            <p>100〜150人<br />400杯/月</p>
          </div>
        </div>
      </div>
    </div>
    <div class="top8" id="featured" v-scroll-reveal.reset="animation">
      <div class="top8-conntent">
        <div class="top8-head">
          <h1>Featured</h1>
          <p>of our Service</p>
        </div>
        <div class="feature">
          <img src="@/assets/img/coffee-been.png" />
          プロ焙煎師厳選の高品質な生豆を使用
        </div>
        <div class="feature">
          <img src="@/assets/img/coffee-been.png" />
          焙煎したての、新鮮のコーヒーを提供
        </div>
        <div class="feature">
          <img src="@/assets/img/coffee-been.png" />
          プロ焙煎師が訪問し、目の前で焙煎
        </div>
        <div class="feature">
          <img src="@/assets/img/coffee-been.png" />
          プロ焙煎師がコーヒーをカスタマイズ
        </div>
        <div class="feature">
          <img src="@/assets/img/coffee-been.png" />
          会社の規模に応じた、サービスプラン
        </div>
      </div>
    </div>
    <div class="top9" id="contact" v-scroll-reveal.reset="animation">
      <div class="top9-up">
        <h1>Contact us</h1>
        <p>
          TEL : 080-4649-0896(代表電話)<br />Mail : coffee.taku.5043@gmail.com
        </p>
      </div>
      <div class="top9-down">
        <div class="top9-img"></div>
      </div>
    </div>
  </div>
</template>
<script src="https://unpkg.com/scrollreveal/dist/scrollreveal.min.js"></script>
<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      ActiveBtn: false,
      animation: { duration: 1000, viewFactor: 0.2, reset: true },
    };
  },
  mounted() {
    let header = document.getElementById("header");
    window.addEventListener("scroll", function() {
      let scroll = window.scrollY;

      if (scroll > 700) {
        header.style.backgroundColor = "rgba(0, 0, 0, 0.5)";
      } else {
        header.style.backgroundColor = "rgba(0, 0, 0, 0)";
      }
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* header */
header {
  width: 100%;
  height: 60px;
  display: block;
  position: fixed;
  display: flex;
  align-items: center;
  justify-content: start;
  background-color: rgba(0, 0, 0, 0);
  z-index: 50;
}
header a {
  text-decoration: none;
  font-size: 3vw;
  color: white;
  padding: 10px;
}
.header-left {
  width: 50%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.header-left a {
  padding-left: 10px;
}
.header-right {
  width: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
.header-right a {
  padding: 5px;
}
header a:hover {
  color: rgba(209, 140, 10, 1);
  transition: all 0.5s;
}
.hamburger_btn {
  display: none;
}
/* top1 */
.top1 {
  background-image: url("/top1-a.png");
  background-size: cover;
  background-attachment: fixed;
  background-position: 50% 50%;
  max-width: 100%;
  height: 100vh;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}
.top1 h1 {
  margin-bottom: 70px;
  font-family: serif;
  text-align: center;
  font-size: 4vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* top2 */
.top2 {
  height: 100vh;
  background-color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.top2-text {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.top2-head {
  color: black;
  text-align: center;
  font-family: serif;
  margin-top: 30px;
  margin-bottom: 30px;
  font-size: 6vw;
}
.top2 p {
  width: 80%;
  font-size: 1.8vw;
  text-align: center;
}
.fa-coffee {
  margin-top: 20px;
  font-size: 40px;
}
.soon {
  color: white;
  font-size: 10vw;
}
.top2-pic {
  margin-top: 20px;
  height: 65vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}
.top2-pic p {
  display: flex;
  align-items: center;
  justify-content: center;
}

.fa-water {
  height: 400px;
  color: rgba(209, 140, 10, 1);
  padding: 50px;
  font-size: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.fa-arrow-down {
  display: none;
  height: 400px;
  color: rgba(209, 140, 10, 1);
  padding: 50px;
  font-size: 40px;
}
.three-coffee {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.three-coffee h2 {
  margin-top: 20px;
  font-size: 40px;
  text-align: center;
  color: black;
}
.kind {
  font-size: 13px;
  color: rgba(209, 140, 10, 1);
}
.coffee-pac {
  background-image: url("/coffee3-cutout.png");
  background-size: cover;
  width: 200px;
  height: 400px;
  position: relative;
  z-index: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.coffee-pac::before {
  content: "";
  position: absolute;
  /* 輪郭がぼやけてしまうのでブラー範囲を広げる */
  top: -5px;
  bottom: -5px;
  left: -5px;
  right: -5px;
  background: inherit;
  filter: brightness(0.5);
  z-index: -1;
}

/* top3 */
.top3 {
  height: 30vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.top3 h1 {
  font-size: 15vw;
  color: rgba(246, 246, 244, 1);
  text-align: center;
}
/* top4 */
/* top5 */
.top5 {
  height: 70vh;
  background-color: rgba(246, 246, 244, 1);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}
.top5-left {
  width: 40%;
  padding-left: 50px;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  flex-direction: column;
}
.top5-left h1 {
  padding-left: 50px;
  color: rgba(159, 121, 81, 1);
  text-align: start;
  font-size: 5vw;
}
.top5-left p {
  padding-left: 50px;
  text-align: start;
  font-size: 1.2vw;
}
.top5-right {
  background-image: url("/baisenn.jpg");
  width: 40%;
  height: 70%;
  margin-left: 30px;
}
/* top6 */
.top6 {
  height: 70vh;
  background-color: rgba(246, 246, 244, 1);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}

.top6-left {
  background-image: url("/top6.png");
  background-size: cover;
  width: 60%;
  height: 80%;
}
.top6-right-flex {
  display: none;
}
.top6-right-nomal {
  width: 40%;
  padding-left: 3%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.top6-right-nomal h1 {
  text-align: start;
  color: rgba(159, 121, 81, 1);
  text-align: start;
  font-size: 5vw;
}
.top6-right-nomal p {
  text-align: start;
  font-size: 1.2vw;
}
/* top7 */
.top7 {
  background: white;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.top7-conntent {
  width: 80%;
  height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
}
.price {
  margin: 7%;
  width: 20%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.price-image1 {
  background-image: url("/price1.png");
  background-size: cover;
  width: 100%;
  height: 60vh;
}
.price-image2 {
  background-image: url("/price2.png");
  background-size: cover;
  width: 100%;
  height: 60vh;
}
.price-image3 {
  background-image: url("/price3.png");
  background-size: cover;
  width: 100%;
  height: 60vh;
}
.price h3 {
  text-align: center;
  padding-top: 20px;
  color: black;
  font-size: 2vw;
}
.price p {
  text-align: center;
  color: rgba(159, 121, 81, 1);
  font-size: 0.8vw;
}
/* top8 */
.top8 {
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.top8-conntent {
  padding: 50px;
  background-color: rgba(246, 246, 244, 1);
  width: 80%;
  height: 80%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.top8-head {
  width: 90%;
  height: 30%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin-bottom: 50px;
}
.top8-head h1 {
  font-size: 5vw;
  color: black;
  text-align: center;
}
.top8-head p {
  font-size: 1.2vw;
  color: black;
  text-align: center;
}
.feature {
  width: 60%;
  margin: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  font-size: 1.2vw;
  color: black;
}
.feature img {
  height: 20px;
  width: 20px;
  margin-right: 20px;
}
/* top9 */
.top9 {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.top9-up {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  text-align: center;
}
.top9-up h1 {
  font-size: 5vw;
  color: black;
}
.top9-up p {
  font-size: 1.2vw;
}
.top9-down {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50%;
  width: 100%;
}
.top9-img {
  background-image: url("/top9.png");
  background-size: cover;
  width: 80%;
  height: 40vh;
}

@media screen and (max-width: 480px) {
  header {
    display: none;
    z-index: 11;
  }
  /*ボタン*/
  .hamburger_btn {
    display: block;
    position: fixed; /*常に最上部に表示したいので固定*/
    top: 0;
    right: 0;
    width: 70px;
    height: 72px;
    cursor: pointer;
    z-index: 50;
  }

  .hamburger_btn .line {
    position: absolute;
    top: 0;
    left: 20px;
    width: 32px;
    height: 2px;
    background: rgba(155, 155, 155, 1);
    text-align: center;
  }

  .hamburger_btn .line_01 {
    top: 16px;
    transition: 0.4s ease;
  }
  .hamburger_btn .line_02 {
    top: 26px;
    transition: 0.4s ease;
  }
  .hamburger_btn .line_03 {
    top: 36px;
    transition: 0.4s ease;
  }

  .btn_line01 {
    transform: translateY(10px) rotate(-45deg);
    transition: 0.4s ease;
  }
  .btn_line02 {
    transition: 0.4s ease;
    opacity: 0;
  }
  .btn_line03 {
    transform: translateY(-10px) rotate(45deg);
    transition: 0.4s ease;
  }

  /*サイドバー*/
  .menu-enter-active,
  .menu-leave-active {
    transition: opacity 0.4s;
  }
  .menu-enter,
  .menu-leave-to {
    opacity: 0;
  }
  .menu-leave,
  .menu-enter-to {
    opacity: 1;
  }

  .menu li {
    list-style: none;
    line-height: 1;
    padding: 1rem;
  }
  .menu {
    background-color: rgba(0, 0, 0, 0.671);
    z-index: 30;
    padding: 2rem 1rem;
    position: fixed;
    width: 20rem;
    height: 100vh;
    top: 0;
    right: 0;
  }
  .menu a {
    color: rgba(255, 255, 255, 1);
    text-decoration: none;
    font-size: 1.2rem;
    padding: 0 2rem;
  }
  .menu ul {
    margin: 1rem;
    padding: 0;
  }
  .top1 h1 {
    font-size: 10vw;
  }
  .big {
    font-size: 60px;
  }
  .top2-head {
    font-size: 7vw;
  }
  .top2-pic {
    border: 1px solid rgba(209, 140, 10, 1);
    display: flex;
    align-items: center;
    justify-content: flex-start;
    flex-direction: column;
    height: 1000px;
    overflow: auto;
  }
  .fa-water {
    height: 30px;
  }
  .water {
    display: none;
  }
  .fa-arrow-down {
    width: 100%;
    text-align: center;
    display: inline-block;
  }
  .top2-pic p {
    font-size: 18px;
  }
  .top5 {
    height: 70vh;
    background-color: rgba(246, 246, 244, 1);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .top5-left {
    padding-left: 0px;
    width: 80%;
  }
  .top5-left h1 {
    padding: 10px;
    padding-left: 0px;
    font-size: 30px;
  }
  .top5-left p {
    padding: 5px;
    font-size: 15px;
    padding-left: 0px;
  }
  .top5-left p span {
    display: none;
  }
  .top5-right {
    width: 80%;
    height: 50%;
  }
  .top6 {
    height: 70vh;
    background-color: rgba(246, 246, 244, 1);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .top6-left {
    background-image: url("/top6.png");
    background-size: cover;
    width: 100%;
    height: 50%;
    padding: 10px;
    margin-bottom: 10px;
  }
  .top6-right-nomal {
    display: none;
  }
  .top6-right-flex {
    height: 50%;
    width: 80%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .top6-right-flex h1 {
    padding-top: 15px;
    text-align: start;
    color: rgba(159, 121, 81, 1);
    text-align: start;
    font-size: 30px;
  }
  .top6-right-flex p {
    padding: 15px;
    text-align: start;
    font-size: 15px;
  }
  .top7 {
    height: 120vh;
  }
  .top7-conntent {
    flex-direction: column;
  }
  .price {
    margin: 0px;
    flex-direction: row;
    height: 40vh;
    width: 90%;
  }
  .price-image1 {
    background-image: url("/price1.png");
    background-size: cover;
    width: 100%;
    height: 40vh;
  }
  .price-image2 {
    background-image: url("/price2.png");
    background-size: cover;
    width: 100%;
    height: 40vh;
  }
  .price-image3 {
    background-image: url("/price3.png");
    background-size: cover;
    width: 100%;
    height: 40vh;
  }
  .price-text h3 {
    padding-left: 12px;
    font-size: 25px;
  }
  .price-text p {
    padding-left: 12px;
    font-size: 18px;
  }
  .top8-conntent {
    width: 100%;
  }
  .top8-head h1 {
    font-size: 30px;
  }
  .feature {
    width: 90%;
    margin: 10px 0 10px 0;
    font-size: 18px;
  }
  .top9-up h1 {
    font-size: 30px;
  }
  .top9-up p {
    font-size: 18px;
  }
}
</style>
