<template>
  <div class="main">
    <div class="test container">
      <img :src="'/logo.png'" alt="demo">
      
    </div>
    
    <div class="test filmin">
      <span id="">
        <h1>REDISEÑO FILMIN</h1>
        <p class="fadein">
          Filmin es una plataforma de video en streaming o bajo demanda que ha crecido enormemente en los últimos meses, sin embargo el diseño de su web necesita un lavado de imagen para generar una navegación más agradable para el usuario.
Con una estética que parte del estándar que ha ido creando Netflix en este campo se ha llevado a cabo un planteamiento que aún en construcción ya refleja el concepto de nueva imagen modernizada pero manteniendo el espíritu clásico de Filmin.
Este proyecto se ha llevado a cabo junto la con la diseñadora Andrea Cascallana.
        </p>
      </span>
    </div>

    <div class="test container">
      <vue-awesome-swiper></vue-awesome-swiper>
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin6.jpg'" alt="demo">
    </div>
    
    <div class="test filmin_image">
      <img :src="'/filmin5.jpg'" alt="demo">
    </div>
    
    <div class="test filmin_image">
      <img :src="'/filmin4.jpg'" alt="demo">
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin3.jpg'" alt="demo">
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin2.jpg'" alt="demo">
    </div>



        <div class="test peru">
      <span id="">
        <h1>LIBRO PERÚ</h1>
        <p class="fadein whitext">
        Este proyecto es algo más personal y en él pretendo mostrar parajes de Perú poco conocidos como reclamo turístico y no solo de esa forma sino de exploración, de sitios menos visitados de mi país.
La narrativa del libro consiste en una descripción del lugar o elemento mostrado y una serie de imágenes que hablan por si solas.
El desarrollo de este proyecto parte de la aplicación de distintas tintas especiales de las cuales he escogido principalmente tonos dorados que son muy representativos del imperio Inca.
        </p>
      </span>
    </div>

    <div class="test peru_image">
      <img :src="'/peru6.jpg'" alt="demo">
    </div>
    
    <div class="test peru_image">
      <img :src="'/peru5.jpg'" alt="demo">
    </div>
    
    <div class="test peru_image">
      <img :src="'/peru4.jpg'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru3.jpg'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru2.jpg'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru1.jpg'" alt="demo">
    </div>



        <div class="test bocal">
      <span id="">
        <h1>REVISTA BOCAL</h1>
        <p class="fadein whitext">
        Bocal es una revista de contenido musical bajo demanda, se publicaría en web pero el cliente siempre podría solicitar su impreso a domicilio.
La premisa de este proyecto era llevar a cabo una mezcla entre periódico y revista con contenido tanto en web como impreso.
Este proyecto se llevó a cabo con el diseñador Antonio Duran y lo que muestro aquí es mi trabajo de maquetación que fue el principal cometido en este trabajo además de la organización del mismo
        </p>
      </span>
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal6.jpg'" alt="demo">
    </div>
    
    <div class="test bocal_image">
      <img :src="'/bocal5.jpg'" alt="demo">
    </div>
    
    <div class="test bocal_image">
      <img :src="'/bocal4.jpg'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal3.jpg'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal2.jpg'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal1.jpg'" alt="demo">
    </div>


    //INPUT
  <div class="test contact">
    <h2>CONTACTO</h2>

    <form action="https://formspree.io/f/xzbygdzo" method="post" class="form_group">
      <label for="name">Nombre</label>
      <input type="text" name="name" value="" placeholder="Pepito Perez">
      <label for="Email">Email</label>
      <input type="text" name="Email" id="email" value="" placeholder="pepitoperez@gmail.com">
      <label for="message">Mensaje</label>
      <textarea name="message" cols="30" rows="10" style="resize: none" placeholder="Deja tu mensaje aquí"></textarea>
      <button type="submit" name="myButton">Enviar</button>
      
    </form>

  </div>


 //FINAL MAIN
  </div>

</template>



<script>
import VueAwesomeSwiper from '../components/VueAwesomeSwiper.vue';
export default {
  components: { VueAwesomeSwiper },
  mounted() {
    const controller = new this.$scrollmagic.Controller();

    var slides = document.querySelectorAll("div.test");

    // create scene for every slide
    for (var i = 0; i < slides.length; i++) {
      new this.$scrollmagic.Scene({
        triggerElement: slides[i],
        triggerHook: 0,
      })
        .setPin(slides[i], { pushFollowers: false })
        //.addIndicators() // add indicators (requires plugin)
        .addTo(controller);
    }

  },
};
</script>
<style lang="scss">

/* 
*{
  border: 1px solid pink;;
} */


.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.filmin {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #02FFA1;
}

.filmin_image {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #02FFA1;
}

.peru {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #FF0A4F;
}

.peru_image {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #FF0A4F;
}

.bocal {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #4FB586;
}

.bocal_image {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #4FB586;
}

.contact{
  margin: 0 auto;
  min-height: 100vh;
  background: #EEEEEE;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-justify: center;
}

.fadein{
  margin: 0 auto;
  max-width: 75vh;
  display: flex;
}

H1{
  font-family: "MerriweatherSans", "San serif";
  font-size: 90px;
  font-weight: 300;
  color: #FFFFFF;
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

H2{
  font-family: "MerriweatherSans", "San serif";
  font-size: 90px;
  color: #424242;
  margin-bottom: 4rem;
  margin-top: 100px;
}

p{
  font-family: "OpenSans", "San serif";
  font-size: 18px;
  color: #424242;
  line-height: 27px;
  text-align: justify;
}

.whitext{
  color: #FFFFFF;
}

.links {
  padding-top: 15px;
}


.form_group{
  display: flex;
  flex-direction: column;
}

//Input styles

form {
	background-color: #EEEEEE;
  width: 37rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

label{
  font-family: "MerriweatherSans", "San serif";
  font-size: 15px;
  color: #424242;
  display: flex;
  align-self: flex-start;
  margin: 1rem 0 0 0;

}

button{
  width: 128px;
  height: 48px;
  border: 4px solid #424242;
  border-radius: 4px;
  background-color: #424242;
  color: #EEEEEE;
  font-family: "MerriweatherSans", "San serif";
  font-size: 16px;
  line-height: 26px;
  letter-spacing: 0.1em;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  align-self: flex-end;
  margin: 1rem 0 0 0;

}

button:hover{
    background-color: #9b9b9b;
    border: 4px solid #9b9b9b;
    color: #424242;
  }


label {}

input[type="text"]{
  font-family: "MerriweatherSans", "San serif";
  background-color: transparent;
  border: 2px solid #424242;
  border-radius: 4px;
  color: #424242;
  width: 596px;
  height: 48px;
  padding: 0 0 0 0.5rem;
  margin: 0 auto;
  margin: 1rem 0 1rem 0;
}

textarea{
  font-family: "MerriweatherSans", "San serif";
  background-color: transparent;
  border: 2px solid #424242;
  border-radius: 4px;
  color: #424242;
  width: 596px;
  height: 254px;
  padding: 1rem 0 0 0.5rem;
  margin: 1rem 0 1rem 0;
}

textarea{
  height: 100%;
  word-break: break-all;
}



/* Swiper */





</style>