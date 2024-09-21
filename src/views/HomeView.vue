<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative;" class="mt-16">
              <h1 class="text-grey">Hola</h1>
              <h1 class="text-grey">Soy Ernesto Vidal</h1>
              <span class="text-grey">Estudiante De Preparatoria</span> <br>
              <v-btn tile dark class="text-blue" variant="outlined">Contactame</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute;z-index: 9999;bottom:0;margin-left:auto;margin-right:0;text-align:center">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999;" class="mt-16">
              <v-img src="../assets/WhatsApp Image 2024-08-24 at 4.04.13 PM.jpeg" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="../assets/fotoer.jpeg" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mt-16">Acerca de Mi</h2>
              <div style="width:120px">
                <v-slider v-model="slider2" color="black" label="">
                </v-slider>
              </div>
              <h4 class="mt-n4">tengo 15 años</h4>
              <h4>información</h4>
              <p class="text-grey">Soy Ernesto Vidal soy de Quintana Roo tengo 15 años actualmente estoy en el grado academico de la preparatoria CECYTE Quintana Roo Plantel 1 en la especialidad de TSMEC.</p>
              <br>
              <p class="text-grey"></p>
              <v-btn tile dark color="blue" class="mt-4">
                Descargar CV
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h1>Lo que hago.</h1>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="black" label="">
          </v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="Portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn color="blue" class="text-white">
                  <v-icon>fas fa-clipboard-check</v-icon>
                </v-btn>
                <h3 class="ml-3 mt-4">Editar Videos</h3>
                <p class="text-grey ml-3 mt-4 text-caption">Soy experto en la edición de video utilizando <br>
                  herramientas avanzadas  como Adobe Premiere y DaVinci Resilve. <br> Asegurando siempre una alta calidad en <br> 
                  la narrativa visual  y en los efectos especiales.
                </p>
              </div>

              <div class="child">
                <v-btn color="blue" class="text-white">
                  <v-icon>fas fa-blog</v-icon>
                </v-btn>
                <h3 class="ml-3 mt-4">Paginas Wed</h3>
                <p class="text-grey ml-3 mt-4 text-caption">Tengo experiencia en el diseño y desarrollo de páginas web responsivas <br> y optimizadas. Utilizo lenguajes como HTML, CSS, y JavaScript</p>
              </div>

              <div class="child">
                <v-btn color="blue" class="text-white">
                  <v-icon>fas fa-place-of-worship</v-icon>
                </v-btn>
                <h3 class="ml-3 mt-4">Emsanbles De PC</h3>
                <p class="text-grey ml-3 mt-4 text-caption">Cuento con conocimientos sólidos en el ensamblaje de computadoras, <br> desde la selección de componentes hasta la configuración del sistema.</p>
              </div>

              
            </v-col>
          </v-row>
          <v-diveder></v-diveder>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="cyan" class="mr-2">Todos</v-btn>
          <v-btn class="mr-2" variant="tonal">Edición de videos</v-btn>
          <v-btn class="mr-2" variant="tonal">Creación de paginas web</v-btn>
          <v-btn class="mr-2" variant="tonal">Emsanble de PC</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-rom class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4" > 
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12 : 2" :class="{'on-hover': isHovering}" v-bind="props">

                  <v-img :src="item.img" height="255px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-rom>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <V-btn color="blue" class="mt-4">
            Conocer mas 
            </V-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-card class="mw-auto" max-width="344" height="">
              <v-img src="../assets/Edicion.jpeg" height="200px" cover></v-img>
              <v-card-title>Edición de Videos</v-card-title>
              <v-card-sibtitle>Video </v-card-sibtitle>
              <v-card-text>Especialista en crear contenido visual impactante, desde la narrativa hasta los efectos especiales. </v-card-text>
            </v-card>
            <v-card class="mw-auto" max-width="344" height="">
              <v-img src="../assets/paginasweb.jpeg" height="200px" cover></v-img>
              <v-card-title>Creación de Paginas Web</v-card-title>
              <v-card-sibtitle>paginas </v-card-sibtitle>
              <v-card-text>Diceño y desarrollo de sitios web responsivos y funcionales, optimizados para todas las plataformas. </v-card-text>
            </v-card>
            <v-card class="mw-auto" max-width="344" height="">
              <v-img src="../assets/Emsanble.jpeg" height="200px" cover></v-img>
              <v-card-title>Ensamble de PC</v-card-title>
              <v-card-sibtitle>Ensamble  </v-card-sibtitle>
              <v-card-text>experto en armar equipos de personalizados de alto rendimiento para diversas necesidades. </v-card-text>
            </v-card>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="biog">
        <dir class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1>Contratame para tus proyectos</h1>
              <p>SI te interesa lo que hago me puedes contactar en la seccion de contactos.</p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="blue" class="mt-15">Contrateame</v-btn>
            </v-col>
          </v-row>
        </dir>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-rom>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Información de contacto</h1>
              <v-icon >fas fa-envelope</v-icon>
              <p class="mb-10">ernestovidal617@gmail.com</p>
              <v-icon>fas fa-phone-volume</v-icon>
              <p class="mb-10">+52 984-180-63-81</p>
              <v-icon>fas fa-map-location</v-icon>
              <p>Calle 68 Nte, Luis Donaldo Colosio, 77728 Playa del Carmen, Q.R.</p>

            </div>
          </v-col>
          <v-col cols="12" sm="6">
            <h1 class="mt-8">Mandame mensaje</h1>
            <v-text-field label="Nombre"></v-text-field>
            <v-text-field label="Telefono"></v-text-field>
            <v-text-field label="Gmail"></v-text-field>
            <v-text-field label="Mensaje"></v-text-field>
            <v-btn color="blue" class="mt-4">Enviar</v-btn>
            <v-divider></v-divider>
            
          </v-col>
        </v-rom>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="blog">
        <v-rom>
          <v-col cols="12" sm="4">
            <div class="chils">
              <h1>Blog</h1>
            </div>
          </v-col>
        </v-rom>
      </v-col>
    </v-container>
  </v-app>
</template>

<style> 
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 365px;
  height: 300px;
  background-color: rgb(13, 106, 149);
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover {
  padding: 0 200px;

}
.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: antiquewhite;
}
.hire {
  width: 100%;
  height: 200%;
  padding:  0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '../components/NavBar.vue';

export default defineComponent({
  name: 'HomeView',
  setup() {
    return {
      slider2: 50,
      items: [
        { img: "yo.jpg" },
      ],
    };
  },

  components: { 
    NavBar,
  },
});
</script>