<template>
  <div>
    <div class="test container">
      <img :src="'/logo.png'" alt="demo">
      
    </div>

    <div class="test container2">
      <span id="">
        <h1>Contenedor 2</h1>
        <p class="fadein">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap into electronic typesetting,
          remaining essentially unchanged. It was popularised in the 1960s with
          the release of Letraset sheets containing Lorem Ipsum passages, and
          more recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </p>
      </span>
    </div>

    <div class="test container3">
      <span id="">Contenedor 3</span>
    </div>

    <div class="test container4">
      <span id="">Contenedor 4</span>
    </div>

    <div class="test container2">
      <span id="">Contenedor 5</span>
    </div>

    <div class="test container3">
      <span id="">Contenedor 6</span>
    </div>

    <div class="test container4">
      <span id="">Contenedor 7</span>
    </div>

    <div class="test container2">
      <span id="">Contenedor 8</span>
    </div>

    <div class="test container3">
      <span id="">Contenedor 9</span>
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
    //*****NOTAA: COMPROBAR SIEMPRE EL TRIGGER PORQUE PUEDE CAMBIARLO TODO */
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
.test {
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.container2 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: salmon;
}

.container3 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: aquamarine;
}
.container4 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: rgb(206, 28, 230);
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: flex;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: flex;
  font-weight: 300;
  font-size: 36px;
  color: #465c74;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  top: 0;
}

.links {
  padding-top: 15px;
}
</style>
