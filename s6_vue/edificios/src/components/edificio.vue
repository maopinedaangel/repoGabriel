<template>
    <div id="div-edificio">
        <h2>{{ nombreEdificio }}</h2>
        <div id="container">
            <img :src="getImgUrl(srcImagenEdificio)" :alt="altImagenEdificio">
            <div>
                <p>País: {{ paisEdificio }}</p>
                <p>Año: {{ anoEdificio }}</p>
                <p>Altura: {{ alturaEdificio }}m</p>
                <p>Descripción: {{ descripcionEdificio }}</p>
            </div>
        </div>
    </div>
</template>



<script>
export default {
    name: 'edificio',
    props: ['nombre', 'pais', 'ano', 'altura', 'descripcion', 'srcImagen', 'altImagen'],
    data () {
        return {
            nombreEdificio: this.nombre,            
            srcImagenEdificio: this.srcImagen,
            altImagenEdificio: this.altImagen,
            paisEdificio: this.pais,
            anoEdificio: this.ano,
            alturaEdificio: this.altura,
            descripcionEdificio: this.descripcion
        }
    },
    methods: {
        getImgUrl: function(pic) {
            return require('../assets/'+ pic)
        },
    },
    created: function() {
        console.log(this.srcImagen)
    }
    
}
</script>


<style scoped>
#div-edificio {
    text-align:justify;
    width: 600px;   
    margin-left: auto;
    margin-right: auto;
    margin-top: 40px;
    margin-bottom: 40px; 
}
h2 {
    text-align: center;
}
img {
    width: 300px;
    margin-right: 20px;
}
#container {
    display: flex;
    justify-content: center;
}
</style>


