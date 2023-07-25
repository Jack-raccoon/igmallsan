<script setup>
import footerComponent from '../components/footerComponent.vue';
import divider from '../components/dividerComponent.vue';
import 'animate.css';
import AOS from 'aos';
import 'aos/dist/aos.css';
</script>

<template>
  <div class="view home" id="home">
    <div class="hero">
      <div class="hero-text">
        <h5 class="animate__animated animate__fadeInDown">Asegura tu suministro de agua</h5>
        <h2 class="animate__animated animate__pulse animate__infinite">¿Problemas con tu bomba de agua?</h2>
        <h1 class="animate__animated animate__lightSpeedInLeft">¡Nosotros te ayudamos! </h1>
        <h3 class="animate__animated animate__rotateInUpLeft">Llámanos y resolveremos tu problema.</h3>
      </div>
      <div class="hero-img animate__animated" data-aos="fade-down">
        <img src="./../assets/Pipeline-maintenance-amico.png" alt="Bombas de agua">
        <a class="link" href="http://www.freepik.com/author/stories">Designed by storyset / Freepik</a>
      </div>
    </div>
    <div class="about" id="about">
      <div class="about-img animate__animated" data-aos="fade-down">
        <img src="./../assets/about-img.jpeg" alt="Bombas de agua">
        <a class="link" href="https://freepik.com/author/">Designed by macrovector / Freepik</a>
      </div>
      <div class="about-text" data-aos="fade-down">
        <h2>¿Quiénes somos?</h2>
        <p>Somos una empresa dedicada a la venta, instalación y mantenimiento de bombas de agua, con experiencia en el
          mercado.</p>
        <p>Contamos con un equipo de profesionales altamente calificados para brindarle un servicio de calidad.</p>
        <p>Trabajamos con las mejores marcas del mercado, garantizando así la calidad de nuestros productos.</p>
      </div>
    </div>
      <div class="divider">
        <divider/>
      </div>

    <div class="services" id="service">
      <h2>Nuestros servicios</h2>
      <div class="services-cards">
        <div data-aos="fade-down" id="service-1">
          <h1>Instalación</h1>
          <p>Ofrecemos un servicio completo de instalación de bombas de agua para hogares, negocios y comunidades.
            Nuestros
            profesionales altamente capacitados aseguran que la instalación se realice de manera rápida y eficiente,
            garantizando la funcionalidad a largo plazo de su sistema de agua.</p>
        </div>
        <div data-aos="fade-down" id="service-2">
          <h1>Mantenimiento</h1>
          <p>Mantenemos tus bombas de agua en óptimo funcionamiento para evitar cualquier interrupción en el suministro de
            agua. Ofrecemos servicios de mantenimiento preventivo y correctivo para asegurar la eficiencia de tus equipos.
          </p>
        </div>
        <div data-aos="fade-down" id="service-3">
          <h1>Reparación</h1>
          <p>Si tu bomba de agua presenta problemas, no dudes en contactarnos. En nuestro servicio de
            reparación, contamos con técnicos especializados y herramientas de última generación para diagnosticar y
            solucionar cualquier falla que presente tu bomba de agua.</p>
        </div>
      </div>
    </div>
    <div class="contact" id="contact">
      <div class="information" data-aos="fade-down">
        <h1>CONTÁCTANOS</h1>
        <img src="../assets/contact.jpg" alt="bombas de agua peru">
      </div>
      <div class="form" data-aos="fade-down">
        <h1>DÉJANOS TU CONSULTA</h1>
        <form action="" class="animate__animated" netlify>
          <div class="top_form">
            <div class="name">
              <label for="name">NOMBRE:</label>
              <input type="text" name="name" id="name">
            </div>
            <div class="email">
              <label for="email">CORREO:</label>
              <input type="email" name="email" id="email">
            </div>
          </div>
          <label for="message">CONSULTA:</label>
          <textarea name="message" id="message" cols="30" rows="10"></textarea>
          <button type="submit"> Enviar</button>
        </form>
      </div>
    </div>
  </div>
  <footer>
    <footerComponent />
  </footer>
</template>

<style>
.link {
  font-size: 0.8rem;
  color: var(--color-link);
  text-decoration: none;
}

.hero {
  width: 80%;
  height: 80vh;
  margin: 0 auto;
  margin-bottom: 20px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.hero-text {
  width: 40vw;
  font-family: 'Poppins', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  word-wrap: break-word;

}

.hero-text h5 {
  color: #25afc7;
  font-size: 1.5rem;
  font-weight: 800;
}

.hero-text h2 {
  color: #ff6868;
  font-size: 2.5rem;
  font-weight: 800;
  line-height: 1.1;
}

.hero-text h1 {
  color: #226df8;
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1;
}

.hero-text h3 {
  color: #25afc7;
  font-size: 1.5rem;
  font-weight: 800;
}

.hero-img {
  width: 40vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  animation-name: fadeIn;
}

.hero-img img {
  width: 100%;
  height: 100%;
}

.about {
  width: 80%;
  margin: 0 auto;
  margin-bottom: 20px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.about-text {
  width: 40vw;
  font-family: 'Poppins', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  word-wrap: break-word;
}

.about-img {
  width: 40vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  animation-name: bounce;
}

.about-img img {
  width: 100%;
  height: 100%;
}

.services {
  padding: 50px 0;
  background-color: #94b9ff;
  margin: 0 auto;
  margin-bottom: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.services h2 {
  font-family: 'Poppins', sans-serif;
  color: #fff;
  font-size: 2.5rem;
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 1rem;
}

.services-cards {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 20px;
  padding: 5rem;
}

.services-cards div {
  background-color: #fff;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.services div i {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.services div h1 {
  font-size: 2rem;
  margin-bottom: 1rem;
  font-weight: 800;
  font-family: 'Poppins', sans-serif;
}

.services div p {
  font-size: 1rem;
  margin-bottom: 1rem;
}

#service-1 {
  transition-delay: 0.2s;
}

#service-2 {
  transition-delay: 0.4s;
}

#service-3 {
  transition-delay: 0.6s;
}

.contact {
  margin: 80px 10vw;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.information {
  width: 40vw;
  margin: auto 50px;
  font-family: 'Poppins', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  word-wrap: break-word;
}

.information h1 {
  color: #226df8;
  font-size: 2rem;
  font-weight: 800;
  line-height: 1;
}

.information ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.information ul li {
  margin-bottom: 1rem;
}

.information img {
  width: 60%;
  height: 60%;
}

.form {
  width: 40vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  animation-name: bounce;
}

.form h1 {
  color: #226df8;
  font-size: 2rem;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 1rem;
}

form {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.top_form {
  margin: auto ;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.name {
  width: 48%;
}

.email {
  width: 48%;
}

form input, form textarea {
  width: 100%;
  padding: 1rem;
  margin-bottom: 0.6rem;
  border: 1px solid #ccc;
  border-radius: 5px;
}
/* focus  */
form input:focus, form textarea:focus {
  outline: none;
  border-color: #226df8;
}

form textarea {
  height: 150px;
}

form button {
  width: 100%;
  padding: 1rem;
  margin-bottom: 0.6rem;
  border: none;
  border-radius: 5px;
  background-color: #226df8;
  color: #fff;
  font-size: 1rem;
  font-weight: 800;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

/*────────────────── 
    media queries
──────────────────*/

@media only screen and (max-width: 1184px) and (min-width: 1024px) {
  .hero-img{
    width: 50vw;
  }
}

@media only screen and (max-width: 1024px) and (min-width: 917px) {

  .hero-img {
    width: 60vw;
    height: 70vh;
  }
}

@media only screen and (max-width: 917px) and (min-width: 767px) {
    .hero-text{
      padding-top: 40px;
      height: 70vh;
    }
    .hero-img {
      width: 70vw;
      height: 60vh;
    }

}

@media only screen and (max-width: 767px){
  .home {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .hero{
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 10px;
  }
  .hero-text{
    padding-top: 40px;
    width: 100%;
  }
  .hero-text h1{
    font-size: 2rem;
  }
  .hero-text h2 {
    font-size: 1.5rem;
  }
  .hero-text h5{
    font-size: 1.5rem;
  }
  .hero-text h3{
    font-size: 1.5rem;
  }
  .hero-img{
    width: 100%;
    height: 40vh;
  }
  .about {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .about img, .about a {
    display: none;
  }
  .about-text{
    width: 100%;
    margin: 40px 10px;
  }
  .about-text h1{
    font-size: 2rem;
  }
  .divider {
    display: none;
  }

  .services {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .services-cards {
    grid-template-columns: 1fr;
    grid-gap: 10px;
    padding: 10px;
  }

  .services-cards div {
    width: 100%;
    margin: 10px 0;
  }

  .services div h1 {
    font-size: 1.5rem;
  }

  .services div p {
    font-size: 1rem;
  }

  .contact{
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .information {
    width: 100%;
    margin: 40px 10px;
  }

  .information img {
    display: none;
  }

  .form {
    width: 100%;
    margin: 40px 10px;
  }

  .form h1 {
    font-size: 2rem;
  }

  .form form {
    width: 100%;
  }
}

</style>