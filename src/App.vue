<template>
  <div id="app">
    <div class="container">
    <nav class="navbar1">
       <li class="">
      <router-link to="/" class="">Accueil</router-link>
       </li>
      <div class="">
        <li class="">
          <router-link to="/tutorials" class="nav-link">Blog</router-link>
        </li>
        <li class="">
          <router-link to="/add" class="nav-link">Contact</router-link>
        </li>
      </div>
    </nav>
    <div class="boxX">
    </div>
    <div class="box-1">
       <div class="title_bar">
         <div class="title_container">
           <h1 class="title_name">Vincent Robert</h1>
           <h2 class="sousTitre">Développeur Web</h2>
          </div>
        </div>
    </div>
    <div class="box-2">
      <div class="side_bar"></div>
    </div>
    <div class="box-3">
      
      
      
      <div class="container2">
       <router-link to="/" class="">
      <div class="window window-1"><p>Projet 1</p></div>
      </router-link>
        <a href="#" class="">
        <div class="window window-2"><p>Projet 2</p></div>
        </a>
         <a href="#" class="">
          <div class="window window-3"><p>Projet 3</p></div>
          </a>
          </div>
    </div>
    <footer class="box-4">
    </footer>
     <div class="container mt-3">
      <router-view />
    </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "app"
};
</script>


<style>
html, body {
  margin: 0px !important;
  padding: 0px !important;
  background-color: #DCDCDC;
 }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
.container{
  display: grid;
  grid-template-columns: [first] 20vw [line2] 60vw [line3] 20vw [end];
  grid-template-rows: [row1-start] 5vw [row1-end] 10vw [third-line] 100vw [third-line] 5vw [last-line];
  overflow: hidden;
 }
 .container2{
  margin-top: 0vw;
  padding-top: 5vw;
  display: grid;
  grid-template-columns: 35vw ;
  grid-template-rows: 15vw 15vw 15vw 15vw ;
  grid-row-gap: 5vw;

  overflow: hidden;
  justify-content: space-around;
 }
 .window-1{
   
   background-color: white;
    grid-column: 1/2;
   grid-row: 1/2;
   
 }
 .window-2{
   background-color: white;
  grid-row: 2/3;
   
 }
.window-3{
   background-color:white;
    grid-column: 1/2;
  grid-row: 3/4;
   
 }
.navbar1{
  /* width: 100vw;*/
  /* height: 5vw; */
  background-color:#DCDCDC;
  
  grid-column: 1/4;
  grid-row: 1/2;

}
.boxX{
  width: 20vw;
  height: 12.36vw;
  border: solid 1vw black;
  background-color: yellow;
  transform: translate(-5vw, 5vw);
   animation-duration: 1.5s;
  animation-timing-function: ease-out; 
  animation-name: slideRL;
}
@keyframes slideRL {
  from {
    margin-left: 100vw;
    width: 100%;
  }

  to {
    margin-left: 0vw;
    width: 100%;
  }
}
.box-1{
  border: 1vw solid black;
  border-left: unset;
    border-right: unset;
  position: relative;
  background-color:red;
  grid-column: 1/4;
  grid-row: 2/3;
  animation-duration: 1.5s;
  animation-timing-function: ease-out; 
  animation-name: slideRL;
}
.box-2{
  border: 1vw solid black;
  
  background-color:darkblue;
  grid-column: 1/2;
  grid-row: 3/4;
  animation-duration: 1.5s;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards; 
  animation-name: slideBT;
}
.box-3{
  
  border-right: 1vw solid black;;
  background-color:white;
  grid-column: 2/3;
  grid-row: 3/4;
  animation-duration: 3s;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards; 
  animation-name: mainBT;
}
@keyframes mainBT {
  from {
    margin-top: 100vw;
    border-top: 1vw solid black;
   
  }
  99%{
    border-top: 1vw solid black;
  }
  to {
     margin-top: 0vw; 
     /* border-top: unset; */
  
  }
}
.window p{
  margin-top: 3.25vw;
  font-size: 5vw;
   /* transform: perspective(0vw) rotateX(90deg); */
  animation-duration: 2s;
  animation-delay: 3s; 
  animation-timing-function: ease-out;
  animation-fill-mode: forwards; 
  animation-name: windowp;
}
@keyframes windowp {
  from {
  opacity: 0;
   
  }
   30%{
      opacity: 0;
   }
 
  to {
     opacity: 1;
     /* margin-top: 0vw;  */
    
  
  }
}
.window{
/* font-size: 9vw; */
 /* perspective: 200px; */
 border: solid 1vw black;
 /* box-shadow: 1vw 1vw 1vw black; */
 border-radius: 0.1vw;
  transform: perspective(0vw) rotateX(90deg);
  animation-duration: 2s;
  animation-delay: 3s; 
  animation-timing-function: ease-out;
  animation-fill-mode: forwards; 
  animation-name: windowTwist;
}
@keyframes windowTwist {
  from {
    /* margin-top: 100vw; */
    transform: rotate3d(1, 2, -1, 180deg);
    background-color: black;
    /* transform: skew(90deg, 20deg); */
   
  }
   /* 50%{
       transform: rotate3d(1, 2, -1, 180deg);
   } */
 
  to {
      transform: rotate3d(0, 0, 0, 360deg);
       background-color: #DCDCDC;
     /* margin-top: 0vw;  */
    
  
  }
}
 /* .title_bar{ */
  /* position: relative;

  z-index: 10;
  width: 100vw;
  height: 10vw;
  background-color:red;
  animation-duration: 1.5s;
  animation-timing-function: ease-out; 
  animation-name: slideRL;
  grid-area: title_bar; */
/* } */
/* @keyframes slideRL {
  from {
    margin-left: 100vw;
    width: 100%;
  }

  to {
    margin-left: 0vw;
    width: 100%;
  }
} */
.title_container{
 text-align: right;
  width:60vw;
  height: 10vw;
}
.title_name{
  margin-top: 0vw; 
  color: black;
  font-size: 5vw;
  text-shadow: .1vw .1vw .5vw black;
  
  animation-duration: 3s;
  animation-timing-function: ease-in-out; 
  animation-name: slideRL;
}
@keyframes slideRL {
  from {
    margin-left: 100vw;
    width: 100%;
  }

  to {
    margin-left: 0vw;
    width: 100%;
  }
}
  

.sousTitre{
  color: white;
  margin-top: -4.5vw;
  font-size: 2.5vw;
  text-shadow:5px 5px 10px black;
  animation-duration: 3s;
  animation-timing-function: ease-in-out;
  animation-name: slideLR;
}
@keyframes slideLR {
  from {
    opacity: 0;
    margin-left: -105vw;
    width: 100%;
  }
  49%{
    opacity: 0;
  }
  50%{
    opacity: 1;
  }

  to {
    margin-left: 0vw;
    width: 100%;
  }
}
.side_bar{
  margin-top: -15vw;

  /* width: 20vw;
  height: 100vw; */
  background-color:blue;
  /* animation-duration: 1.5s;
  animation-timing-function: ease-out;
   animation-fill-mode: forwards; 
  animation-name: slideBT; */
  
 
}
@keyframes slideBT {
  from {
    margin-top: 100vw;
   
  }
 
  to {
     margin-top: -15vw; 
  
  }
}
 footer{
  /* width: 100vw;
  height: 5vw; */
  
  background-color:grey;
   grid-column: 1/4;
   grid-row: 4/5;
} 
</style>
