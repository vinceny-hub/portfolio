<template>
  <div id="app">
    <div class="container">
    <nav class="navbar1">
      <router-link to="/" class="">Accueil</router-link>
      <div class="">
        <li class="">
          <router-link to="/tutorials" class="nav-link">Blog</router-link>
        </li>
        <li class="">
          <router-link to="/add" class="nav-link">Contact</router-link>
        </li>
      </div>
    </nav>
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
      <div class="window window-1"><p>Projet 1</p></div>
        <div class="window window-2"><p>Projet 2</p></div>
          <div class="window window-3"><p>Projet 3</p></div>
          </div>
    </div>
    <footer class="box-4">
    </footer>

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
  grid-template-rows: 15vw 15vw 15vw ;
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
.box-1{
  position: relative;
  background-color:red;
  grid-column: 1/4;
  grid-row: 2/3;
  animation-duration: 1.5s;
  animation-timing-function: ease-out; 
  animation-name: slideRL;
}
.box-2{
  background-color:black;
  grid-column: 1/2;
  grid-row: 3/4;
  animation-duration: 1.5s;
  animation-timing-function: ease-out;
  animation-fill-mode: forwards; 
  animation-name: slideBT;
}
.box-3{
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
   
  }
 
  to {
     margin-top: 0vw; 
  
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
 border: solid 0.5vw black;
 border-radius: 1vw;
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
  margin-top: 1vw; 
  color: black;
  font-size: 5vw;
  
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
  background-color:black;
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
