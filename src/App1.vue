<template>
  <div id="app">
    <div class="container">
    <nav class="navbar navbar-expand navbar-dark bg-dark">
      <router-link to="/" class="navbar-brand">Accueil</router-link>
      <div class="navbar-nav mr-auto">
        <li class="nav-item">
          <router-link to="/tutorials" class="nav-link">Blog</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/add" class="nav-link">Contact</router-link>
        </li>
      </div>
    </nav>
    <section>
      <div class="title_bar"><div class="title_container"><h1 class="title_name">Vincent Robert</h1><h2 class="sousTitre">Développeur Web</h2></div></div>      
    </section> 
    <section>
      <div class="side_bar"></div>
    </section>

    <footer>
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
  grid-template-areas: 
    "header header header"
    "title_bar title_bar title_bar "
    "side_bar . ."
    "footer footer footer"
    ;
}

.navbar{
  width: 100vw;
  height: 5vw;
  background-color:grey;
  grid-area: header;
}
.title_bar{
  position: relative;
  /* margin-top: -4.3vw; */
  z-index: 10;
  width: 100vw;
  height: 10vw;
  background-color:red;
  animation-duration: 1.5s;
  animation-timing-function: ease-out; 
  animation-name: slideRL;
  grid-area: title_bar;
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
.title_container{
 text-align: right;
  width:60vw;
  height: 10vw;
}
.title_name{
  padding-top: 0.45vw;
  color: black;
  font-size: 5vw;
  /* animation-delay: 3s; */
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
    margin-left: -105vw;
    width: 100%;
  }

  to {
    margin-left: 0vw;
    width: 100%;
  }
}
.side_bar{
  margin-top: 0vw;
  /* position:relative; */
  width: 20vw;
  height: 100vw;
  background-color:black;
  animation-duration: 1.5s;
  animation-timing-function: ease-out;
   animation-fill-mode: forwards; 
  animation-name: slideBT;
  grid-area: side_bar;
 
}
@keyframes slideBT {
  from {
    margin-top: 100vw;
    /* height: 0%; */
  }
   /* 50%{height: 50%;} */
  to {
     margin-top: -15vw; 
    /* height: 100%; */
  }
}
footer{
  width: 100vw;
  height: 5vw;
  background-color:grey;
}
</style>
