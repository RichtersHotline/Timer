<template>
    <div class="container-fluid" id="BG">
        <h2 class="" id="Greeter"></h2>
        <div class="container-fluid" id="Windows">
          <div id="DoorOut" class="Door">
           <div class="DoorDetails">
            
           </div>
          </div>
          
      <div id="WindowID" class="Window">
        
<div id="Out" class="Outside">
  
  <div id="RoofID" class="Roof2">
</div>

  <div class="Pane1"></div>
  <div class="PaneH"></div>

  <div class="Pane2"></div>
  <div class="PaneB"></div>
  
  <!-- <div class="Build">
<div class="Building"></div>
<div class="Building"></div>
<div class="Building"></div>

</div> -->



</div>

<div id="Objs" class="ObjectCon">
<div id="Objects">
<div class="Cup">C</div>
<div class="plate"></div>
<div class="plate2"></div>

<div class="Cup2">C</div>

</div>
<div id="Objects">
<div class=" mt-3 book"></div>
</div>
<div id="Objects">
<div class="Cup text-end">ↄ</div>
<div class="plate"></div>
<div class="plate2"></div>

<div class="Cup2 text-end ">ↄ</div>

</div>


</div>

<div class="OnTable">

</div>

      </div>
      
      <!-- Right Side of Wall -->
 <div class="p-3"></div>
    </div>
    
<!-- <div class="TimerContent ">
<h4 id="Timer"></h4>
<button class="BtnStarter" id="Stopper" @click.prevent="Click">Click to start</button>
</div> -->

    </div>
   
    <div class="container-fluid" id="BG2">
      
    </div>
    <div class="ShadowFlex">
    <div class="container-fluid" id="BGShadow">
    </div>
    <div class="People"></div>

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
    <div class="People"></div>

  </template>
  <script>
  export default {
data() {



},
mounted() {
   let current = new Date().getHours()
   let ODoor = document.getElementById("Greeter")
   let Objects = document.getElementById("Objs")
   let Greeting = ""
   if (current < 12) {
    Greeting = "Good Morning"
    ODoor.innerHTML = Greeting +  "🌅"
    ODoor.style.setProperty("color", "orange", "important")
   }
   else if (current < 18) { 
    Greeting = "Good Afternoon"
    ODoor.innerHTML = Greeting +  "🌇"
    ODoor.style.setProperty("color", "orange", "important")
    document.body.style.setProperty("background-color",  "#4A1C02", "important")

   }
   else {

    Greeting = "Good Night..."
    ODoor.innerHTML = Greeting +  "🌃"
    ODoor.style.setProperty("color", "#49468a", "important")
    document.body.style.setProperty("background-color",  "#070200", "important")
    Objects.style.display = "none"
    document.body.style.filter = "brightness(20%)"
    document.getElementById("Out").style.backgroundImage = "linear-gradient(0deg, rgba(4,6,34,1) 0%, rgba(0,0,0,1) 100%)"
    document.getElementById("DoorOut").style.backgroundImage = "linear-gradient(00deg, rgba(4,6,34,1) 0%, rgba(0,0,0,1) 100%)"
    document.getElementById("BGShadow").style.display = "none"
    document.getElementById("BG2").style.backgroundColor = "#2f1607"
    document.getElementById("WindowID").style.border ="12px inset #2E1005"
    document.getElementById("RoofID").style.backgroundColor = "#170b04"
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