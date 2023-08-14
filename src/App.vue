<template>
  <header>
    <input type="checkbox" name="" id="toggler">
    <label for="toggler" class="fas fa-bars"></label>

    <a href="#" class="logo"><i class="fa-solid fa-newspaper fa-beat"></i></a>

    <nav class="navbar">
      <router-link to="/">Headlines</router-link>
      <router-link to="/about">Articles</router-link>
    </nav>
    <div class="icons">
      <i class="fa-solid fa-heart fa-beat"></i>
      <i class="fa-solid fa-user fa-beat"></i>
    </div>
  </header>
  <router-view/>
  <Footer/>
</template>

<script>
import Footer from './components/Footer.vue';

export default {
  components: {
   Footer
  }
}
</script>
<style>
#app {
  font-family: Georgia, 'Times New Roman', Times, serif;
  font-size: 62.5%;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
  text-align: center;
  margin-top: 125px;
}
:root{
 --purple: #A020F0
}
*{
  margin: 0; padding: 0;
  box-sizing: border-box;
  font-family: Georgia, 'Times New Roman', Times, serif;
  outline: none; border: none;
  text-decoration: none;
  text-transform: capitalize;
  transition: .2s linear;
}

header{
  position:fixed;
  top:0; left:0; right:0;
  background: #A020F0;
  padding: 1rem 9%;
  display:flex;
  align-items:center;
  justify-content: space-between;
  z-index: 1000;
}

header .logo{
  font-size: 3rem;
  color:#333;
  font-weight: bolder;
}

header .navbar a{
  font-size: 2rem;
  padding: 0 1.5rem;
  color: #fff;
}

header .navbar a:hover{
  color: 	#BF40BF;
}

header .icons i{
  font-size: 2.5rem;
  margin-left: 1.5rem;
}

header .icons i:hover{
  color: #BF40BF;
}

header #toggler{
  display: none;
}

header .fa-bars{
  font-size: 3rem;
  color: #fff;
  border-radius: .5rem 1.5rem;
  cursor: pointer;
  display: none;
}
@media (max-width:991px) {
  #App{
    font-size:55%;
  }
  header{
    padding:2rem;
  }
}
@media (max-width:768px){
  header .fa-bars{
    display: block;
  }
  header .navbar{
    position: absolute;
    top:10; left:0; right:0;
    

  }
}

</style>
