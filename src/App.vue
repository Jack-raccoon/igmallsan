<script setup>
import { RouterLink, RouterView } from 'vue-router'

const toggleMenu = () => {
  const nav = document.querySelector('.nav-bar')
  const menu = document.querySelector('.menu')
  const bg = document.querySelector('.bg')
  nav.classList.toggle('nav-active')
  menu.classList.toggle('toggle')
  bg.classList.toggle('bg-active')
}

window.onload = () => {
  const menu = document.querySelector('.menu')
  menu.addEventListener('click', toggleMenu)
}

</script>

<template>
  <header>
    <img alt="IGMallsan logo" class="logo" src="@/assets/logo.jpg" width="180" height="85" />
      <nav>
        <ul class="nav-bar">
          <div class="bg"></div>
          <li class="nav-link active"><RouterLink to="/">INICIO</RouterLink></li>
          <li class="nav-link"><RouterLink to="/about">EMPRESA</RouterLink></li>
          <li class="nav-link"><RouterLink to="/products">PRODUCTOS</RouterLink></li>
          <li class="nav-link"><RouterLink to="/services">SERVICIOS</RouterLink></li>
          <li class="nav-link"><RouterLink to="/contact">CONTACTO</RouterLink></li>
        </ul>
        <div class="menu">
          <div class="line1"></div>
          <div class="line2"></div>
          <div class="line3"></div>
        </div>
      </nav>
  </header>
    <RouterView />
    
  <div class="wsp">
    <a href="https://api.whatsapp.com/send?phone=+51990460089&text=Hola%20IGMallsan%20estoy%20interesado%20en%20sus%20productos" target="_blank">
      <i class="fa-brands fa-whatsapp" style="color: #fff;"></i>
    </a>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12);
  position: fixed;
  padding: 0 14rem;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1;
  display: flex;
  flex-direction: row;
}

.logo{
  margin-left: 2rem;
}

nav {
  margin-left: auto;
  margin-right: 2rem;
  display: flex;
  flex-direction: row;
  align-items: center;
}

nav ul {
  display: flex;
  flex-direction: row;
  list-style: none;
  margin: 0;
  padding: 0;
}

nav li {
  margin: 0 1rem;
}
.wsp {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 100;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background-color: #25d366;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12);
}

.wsp a {
  color: #fff;
  font-size: 2.5rem;
}

/*────────────────── 
    scroll
──────────────────*/

::-webkit-Scrollbar {
    width: 5px;
    background: rgba(5, 5, 5, 1);
}

::-webkit-Scrollbar-thumb {
    border-radius: 10px;
    background: var(--main-decor-color);
    box-shadow: inset 0 0 20px var(--main-decor-color);
}

::-webkit-Scrollbar-track {
    margin-top: 80px;
    border-radius: 10px;
}

/*────────────────── 
    menu
──────────────────*/

.menu {
  display: none;
}

.menu div {
  width: 25px;
  height: 3px;
  background-color: #0565e2;
  margin: 5px;
  transition: all 0.3s ease;
}

.toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
}

.toggle .line2 {
    opacity: 0;
}

.toggle .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
}

@keyframes navLinkFade {
    from {
        opacity: 0;
        transform: translatex(50px);
    }

    to {
        opacity: 1;
        transform: translatex(0px);
    }
}

/*────────────────── 
    media queries
──────────────────*/

@media only screen and (max-width: 1184px) and (min-width: 1024px) {
  header {
    padding: 0 7rem;
  }
}

@media only screen and (max-width: 1024px) and (min-width: 917px) {
  header {
    padding: 0 4rem;
  }
}

@media only screen and (max-width: 917px) and (min-width: 767px) {
  header {
    padding: 0;
  }
}

@media only screen and (max-width: 767px){
  header {
    padding: 0 2rem;
  }
  .logo {
    margin-left: 0;
  }
  .nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12);
    padding: 0 1rem;
  }
  
  .logo {
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
    z-index: 3;
  }

  .nav-show {
    opacity: 1;
  }

  .menu {
    position: absolute;
    display: block;
    right: 1rem;
    cursor: pointer;
    z-index: 5;
  }

  .nav-bar {
    position: fixed;
    top: 0px;
    right: 0;
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    background: #fff;
    transform: translatex(100%);
    transition: transform 0.5s ease-in;
    z-index: 2;
  }

  .nav-bar li {
    opacity: 3;
  }

  main {
    margin-top: 80px;
  }

  .wsp {
    z-index: 0;
  }

}

@media only screen and (max-width: 360px) {
  header {
    padding: 0;
  }
  
  nav {
    margin: auto;
  }
  .nav-bar {
    padding: 0;
  }

  .menu {
    left: 0;
    right: 0;
  }
}

.nav-active {
  transform: translatex(0%);
}

</style>
