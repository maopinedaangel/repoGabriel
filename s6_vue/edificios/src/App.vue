<template>
  <div id="app">
    <menubar />
    <!--
    <img src="./assets/logo.png">
    <HelloWorld/>
    -->    
    <edificio v-for="k in edificios" :nombre="k.nombre" :pais="k.pais" :ano="k.ano" :altura="k.altura" :descripcion="k.descripcion" :srcImagen="k.srcImagen" :altImagen="k.altImagen" :key="k" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import edificio from './components/edificio'
import menubar from './components/menubar'

export default {
  name: 'App',
  components: {
    HelloWorld,
    edificio,
    menubar
  },
  data: function() {
    return {
      edificios: [
        {
          nombre: "Burj Khalifa", 
          pais: "Emiratos Árabes Unidos",
          ano: 2010,
          altura: 828,
          descripcion: "Con 828 metros de altura, es la estructura más alta de la que se tiene registro en la historia. Conocido durante su construcción como Burj Dubái (Torre Dubái), el Burj Khalifa es la parte central de un desarrollo conocido como Downtown Dubai, un complejo de 2 km² situado junto a la avenida Jeque Zayed, que atraviesa transversalmente la ciudad de Dubái. La construcción comenzó el 6 de enero de 2004, siendo su inauguración oficial el 4 de enero de 2010. Debe su nombre al Jeque y presidente de los Emiratos Árabes Unidos, Jalifa bin Zayed Al Nahayan.",
          srcImagen: "burj-khalifa.jpg",
          altImagen: "Imagen del Burj Khalifa"
        },
        {
          nombre: "Shanghai Tower", 
          pais: "China",
          ano: 2015,
          altura: 632,
          descripcion: "Es un rascacielos ubicado en el distrito de Pudong en Shanghái, China. El edificio se eleva 632 metros sobre el suelo, con 128 pisos y una superficie de 420 000 m². Es actualmente el edificio más alto de China y el segundo rascacielos más alto del mundo, siendo solamente superado por el Burj Khalifa de Dubái",
          srcImagen: "shanghai-tower.jpg",
          altImagen: "Imagen del Shanghai Tower"          
        },
        {
          nombre: "Makkah Royal Clock Tower", 
          pais: "Arabia Saudita",
          ano: 2011,
          altura: 601,
          descripcion: "Es el edificio más alto en Arabia Saudita y el tercer rascacielos más alto del mundo, tras el Burj Khalifa y la Torre de Shanghái. Es también, por superficie, el tercer edificio más grande del mundo, con un total aproximado de 1 580 000 m². La estructura está ubicada al otro lado de la calle de entrada al Masjid al-Haram, en cuyo interior se encuentra la Kaaba, considerada por los musulmanes el lugar más santo del mundo.",
          srcImagen: "makkah-royal-clock-tower.jpg",
          altImagen: "Imagen del Makkah Royal Clock Tower"           
        },  
                  
      ]
    }
  }
}


</script>

<style>
* {
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
