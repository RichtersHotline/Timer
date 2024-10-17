<template>
    <div class="container-fluid" id="BG">
        <h2 id="Greeter"></h2>
        <div class="container-fluid" id="Windows">
      <div class="Window">
<div class="Outside">
  <!-- <div class="WindowBuilding"></div> -->

<!-- <div class="Build">
<div class="Building"></div>
<div class="Building"></div>
<div class="Building"></div>

</div> -->

  <div class="Roof">

  </div>
  <div class="Floor">
    
  </div>
</div>

      </div>
    
    </div>
    
<!-- <div class="TimerContent ">
<h4 id="Timer"></h4>
<button class="BtnStarter" id="Stopper" @click.prevent="Click">Click to start</button>
</div> -->

    </div>
   
    <div class="container-fluid" id="BG2">
    </div>
    <div class="container-fluid" id="BGShadow">
    </div>

    <div class="container-fluid" id="BG3">
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>
    <div class="Boards"></div>

    </div>
  </template>
  <script>
  export default {
data() {



},
mounted() {
   let current = new Date().getHours()
   let Greeting = ""
   if (current < 12) {
    Greeting = "Good Morning"
    document.getElementById("Greeter").innerHTML = Greeting +  "🌅"

   }
   else if (current < 18) { 
    Greeting = "Good Afternoon"
    document.getElementById("Greeter").innerHTML = Greeting +  "🌇"

   }
   else {

    Greeting = "Good Evening"
    document.getElementById("Greeter").innerHTML = Greeting +  "🌃"
   }

},
methods: {

 Click() {
    // let isClicked = true;
   let seconds = 20
   let Background = document.getElementById("BG")
   let CD = setInterval(function() {
document.getElementById("Timer").innerHTML = "0:" + seconds
    seconds--
   switch(seconds) {
  case -1: 
  clearInterval(CD) 
  console.log("ended")
  document.getElementById("Stopper").innerHTML = "Restart Timer"
  Background.classList.add("Animation3")

  break; 
  case 9:
    console.log("Halfway")
    Background.classList.add("Animation2")


   }
   if (seconds > 0) {
    
    document.getElementById("Stopper").innerHTML = "Stop Timer"
    // Background.classList.add("Animation1")


   }
}, 1000)

 }

   }

}




</script>