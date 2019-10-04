<template>
  <div id="home">
    <div id="app"></div>
    <div class="idx"><div id="c1"></div></div>
    <div class="idx"><div id="c2"></div></div>
    
  </div>
</template>

<style>
.idx{
  height:100vh;
  width:100vw;
  position:relative;
}
#c1{
  width:500px;
  height:500px;
  position:absolute;
  left:50%;
  top:50%;
  border-radius:47%;
  background:#acacac8f;
  animation-name: rotate;
animation-iteration-count: infinite;
animation-timing-function: linear;
animation-duration:10s;
}
#c2{
  width:300px;
  height:300px;
  position:absolute;
  left:10%;
  top:20%;
  border-radius:47%;
  background:rgb(194, 7, 94);
  animation-name: rotate;
animation-iteration-count: infinite;
animation-timing-function: linear;
animation-duration:10s;
}
#app {
height:100vh;
width:100vw;
position: fixed;

align-items: center;

min-height: 100vh;

background-color: rgb(118, 218, 255);

overflow: hidden;
background-attachment:fixed;
z-index:-1
}

#app::before, #app::after {

content: "";

position: absolute;

left: 50%;

min-width: 300vw;

min-height: 300vw;

background-color: #fff;

animation-name: rotate;

animation-iteration-count: infinite;

animation-timing-function: linear;

}

#app::before {

bottom: 15vh;

border-radius: 45%;

animation-duration: 10s;

}

#app::after {

bottom: 12vh;

opacity: .5;

border-radius: 47%;

animation-duration: 10s;

}


@keyframes rotate {

0% {

transform: translate(-50%, 0) rotateZ(0deg);

}

50% {

transform: translate(-50%, -5%) rotateZ(180deg);

}

100% {

transform: translate(-50%, 0) rotateZ(360deg);

}

}
</style>

