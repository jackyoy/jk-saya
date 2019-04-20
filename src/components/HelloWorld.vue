<template>
  <div class="hello">
    <div class="text">
      <h1>{{ msg }}</h1>
      <p>本站是以Vue.js框架製作的SPA網站，純粹做練習用。</p>
      <h3>以下呈現Google提供的免費字體</h3>
      <div class="googlefont-style-1">
        <h3>
          圓體字型
          <br>
        </h3>
        <p>同樣16px，可以明顯感覺到比較小</p>
      </div>
      <div class="googlefont-style-2">
        <h3>
          仿宋體字型
          <br>
        </h3>
        <p>一樣，同樣的像素之下，都比標準字體還小</p>
      </div>
      <div class="googlefont-style-3">
        <h3>
          黑體（思源黑體）
          <br>
        </h3>
        <p>這個字型就比較正常了，至少眼睛不會那麼吃力</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url(https://fonts.googleapis.com/earlyaccess/cwtexyen.css);
@import url(https://fonts.googleapis.com/earlyaccess/cwtexfangsong.css);
@import url(https://fonts.googleapis.com/earlyaccess/notosanstc.css);

.text {
  background-color: white;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.googlefont-style-1 {
  font-family: "cwTeXYen", sans-serif;
}
.googlefont-style-2 {
  font-family: "cwTeXFangSong", serif;
}
.googlefont-style-3 {
  font-family: "Noto Sans TC", sans-serif;
}

@media screen and (max-width: 480px) {
  a {
    padding: 5px;
  }
}

@media screen and (max-width: 768px) {
  a {
    padding: 10px;
  }
}

@media screen and (min-width: 768px) and (max-width: 992px) {
  a {
    padding: 15px;
  }
}
@media screen and (min-width: 992px) {
  .hello {
    margin: 0px 200px 0 200px;
    padding: 10px;
  }
  .text {
    padding: 10px;
    margin: 10px 10px 10px 10px;
    border-radius: 15px;
    -moz-border-radius: 15px;
    background-color: white;
  }
}

@media screen and (min-width: 1200px) {
  .hello {
    margin: 0px 400px 0 400px;
    padding: 10px;
  }
  .text {
    padding: 10px;
    margin: 10px 10px 10px 10px;
    border-radius: 15px;
    -moz-border-radius: 15px;
    background-color: white;
  }
}
</style>
