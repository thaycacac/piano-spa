<template>
  <div>
    <ul>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white special"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
      <li class="black"></li>
      <li class="white"></li>
    </ul>
    <audio class="keyA" src="../assets/E4.mp3"></audio>
  </div>
</template>

<script>
export default {
  mounted(){
    window.addEventListener('keydown', (e) => {
      const audio = document.querySelector('.keyA')
      console.log(audio);
      if(!audio) return;
      audio.currentTime = 0
      audio.play()
    })
  }
};
</script>
<style scoped lang="scss">
main {
  text-align: center;
}
ul {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  list-style: none;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  overflow: hidden;
  padding-left: 1.75vw;
  padding-bottom: 1em;
}
.special {
  margin-right: 27px;
}
.white {
  background: -webkit-linear-gradient(110deg, #333, #000, #333);
  background: linear-gradient(
    -20deg,
    rgb(255, 255, 255),
    rgb(204, 204, 204),
    rgb(223, 223, 223)
  );
  border: 1px solid #ccc;
  border-radius: 0 0 3px 3px;
  box-shadow: inset 0 1px 0 #fff, inset 0 -1px 0 #fff, inset 1px 0 0 #fff,
    inset -1px 0 0 #fff, 0 4px 3px rgba(0, 0, 0, 0.7);
  height: 40vh;
  width: 5vw;
  margin-left: -2vw;
}
.white:nth-child(12n + 6),
.white:nth-child(12n + 13) {
  margin: 0;
}
.white:active {
  box-shadow: 0 2px 2px rgba(0, 0, 0, 0.4);
}
.black {
  background: -webkit-linear-gradient(110deg, #333, #000, #333);
  background: linear-gradient(-20deg, #333, #000, #333);
  border-color: #666 #222 #111 #555;
  border-radius: 0 0 2px 2px;
  border-style: solid;
  border-width: 1px 2px 7px;
  box-shadow: inset 0 -1px 2px hsla(0, 0%, 100%, 0.4),
    0 2px 3px rgba(0, 0, 0, 0.4);
  height: 25vh;
  position: relative;
  width: 3.5vw;
  margin-left: -1.75vw;
  z-index: 1;
}
.black:active {
  border-bottom-width: 2px;
  box-shadow: inset 0 -1px 1px hsla(0, 0%, 100%, 0.4),
    0 1px 0 rgba(0, 0, 0, 0.7), 0 2px 2px rgba(0, 0, 0, 0.4), 0 -1px 0 #000;
}
</style>
