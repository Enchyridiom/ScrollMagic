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

    <div class="test filmin_image">
      <img :src="'/filmin6.png'" alt="demo">
    </div>
    
    <div class="test filmin_image">
      <img :src="'/filmin5.png'" alt="demo">
    </div>
    
    <div class="test filmin_image">
      <img :src="'/filmin4.png'" alt="demo">
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin3.png'" alt="demo">
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin2.png'" alt="demo">
    </div>

    <div class="test filmin_image">
      <img :src="'/filmin1.png'" alt="demo">
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
      <img :src="'/peru6.png'" alt="demo">
    </div>
    
    <div class="test peru_image">
      <img :src="'/peru5.png'" alt="demo">
    </div>
    
    <div class="test peru_image">
      <img :src="'/peru4.png'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru3.png'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru2.png'" alt="demo">
    </div>

    <div class="test peru_image">
      <img :src="'/peru1.png'" alt="demo">
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
      <img :src="'/bocal6.png'" alt="demo">
    </div>
    
    <div class="test bocal_image">
      <img :src="'/bocal5.png'" alt="demo">
    </div>
    
    <div class="test bocal_image">
      <img :src="'/bocal4.png'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal3.png'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal2.png'" alt="demo">
    </div>

    <div class="test bocal_image">
      <img :src="'/bocal1.png'" alt="demo">
    </div>


    //TEMPLATE INPUT. HAY QUE MONTARLO

    <div class="test contact">
      <img :src="'/contact1.png'" alt="demo">
    </div>

    <div class="test contact">
      <img :src="'/contact2.png'" alt="demo">
    </div>



    
  </div>
</template>

<script>
export default {
  mounted() {
    const controller = new this.$scrollmagic.Controller();


//ANIMACIONES POR DEFECTO LOURDES


    var scene = new this.$scrollmagic.Scene({ triggerElement: ".container2" })
      // trigger a TweenMax.to tween
      .setTween("#animate1", 0.5, {
        backgroundColor: "white",
        scale: 2.5,
        rotate: 360,
      })
      .addTo(controller);

    var scene2 = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
      duration: 300,
    })
      // trigger a TweenMax.to tween
      .setPin("#animate2")
      // add indicators (requires plugin)
      //.addIndicators({name: "1 (duration: 300)"})
      //.setTween("#animate2", 0.5, {backgroundColor: "white"})
      .addTo(controller);

  

   //PRUEBA DE FADE IN EN TEXTO. RESULTADO: NO FUNCIONA BIEN, HAY QUE DEFINIR MEJOR LOS PARÁMETROS.
   // ES POSIBLE QUE SE RESUELVA USANDO CSS ADEMÁS DE SCROLLMAGIC 

    var scene2 = new this.$scrollmagic.Scene({
      triggerElement: ".fadein",
      reverse: false,
      triggerHook: 0,
    })

       .setPin(".fade")
       .addTo(controller);

  // TERMINAR PRUEBA DE TEXTO FADE IN



    //PRUEBA DE SECTION WIPES NATURAL. RESULTADO: FUNCIONA BIEN
    //*****NOTA: COMPROBAR SIEMPRE EL TRIGGER PORQUE PUEDE CAMBIARLO TODO */
    ///// triggerHook define la posición del trigger, está va desde 0 siendo este el top hasta 1 que sería el botton

    // get all slides
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
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #FFFFFF;
}

.fadein{
  margin: 0 auto;
  max-width: 75vh;
  display: flex;
}

H1{
  font-family: "MerriweatherSans", "San serif";
  font-size: 80px;
  font-weight: 300;
  color: #FFFFFF;
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
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
</style>
