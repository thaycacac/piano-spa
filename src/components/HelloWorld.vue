<template>
  <div>
    <ul>
      <li class="white KeyA"></li>
      <li class="black KeyW"></li>
      <li class="white KeyS"></li>
      <li class="black KeyE"></li>
      <li class="white KeyD"></li>
      <li class="black KeyR"></li>
      <li class="white special KeyF"></li>
      <li class="white KeyG"></li>
      <li class="black KeyT"></li>
      <li class="white KeyH"></li>
      <li class="black KeyU"></li>
      <li class="white KeyJ"></li>
      <li class="white KeyK"></li>
      <li class="black KeyI"></li>
      <li class="white KeyL"></li>
      <li class="black KeyO"></li>
      <li class="white Semicolon"></li>
      <li class="black KeyP"></li>
      <li class="white Quote"></li>
    </ul>
    <audio class="KeyA"  preload='none'>
      <source src="../assets/e4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyS">
      <source src="../assets/g4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyD">
      <source src="../assets/a4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyF">
      <source src="../assets/b4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyG"  preload='none'>
      <source src="../assets/c5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyH">
      <source src="../assets/d5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyJ">
      <source src="../assets/e5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyK">
      <source src="../assets/f5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyL">
      <source src="../assets/g5.mp3" type="audio/mpeg">
    </audio>
    <audio class="Semicolon">
      <source src="../assets/a5.mp3" type="audio/mpeg">
    </audio>
    <audio class="Quote">
      <source src="../assets/b5.mp3" type="audio/mpeg">
    </audio>

    <audio class="KeyW">
      <source src="../assets/f4g4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyE">
      <source src="../assets/g4a4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyR">
      <source src="../assets/a4b4.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyT">
      <source src="../assets/c5d5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyU">
      <source src="../assets/d5e5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyI">
      <source src="../assets/f5g5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyO">
      <source src="../assets/g5a5.mp3" type="audio/mpeg">
    </audio>
    <audio class="KeyP">
      <source src="../assets/a5b5.mp3" type="audio/mpeg">
    </audio>
  </div>
</template> 

<script>
export default {
  mounted() {
    window.addEventListener("keydown", e => {
      const audio = document.getElementsByClassName(e.code);
      audio[1].play();
      audio[0].classList.add("presskey");
      setInterval(function() {
        audio[0].classList.remove("presskey");
      }, 400);
    });
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
  margin-right: 20px;
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
.presskey {
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
.press-black {
  border-bottom-width: 2px;
  box-shadow: inset 0 -1px 1px hsla(0, 0%, 100%, 0.4),
    0 1px 0 rgba(0, 0, 0, 0.7), 0 2px 2px rgba(0, 0, 0, 0.4), 0 -1px 0 #000;
}
</style>
