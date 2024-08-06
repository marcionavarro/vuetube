<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Olá,</h1>
              <h1 class="text-grey">Eu sou Marcio Navarro</h1>
              <span class="text-gry">Web Designer & Developer</span><br />
              <v-btn tile dark class="text-yellow mt-8" variant="outlined">Contate-me</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="position: absolute; z-index: 9999; bottom: -0; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
              <v-icon>fa fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999;" class="mt-16">
              <v-img src="i1.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="i2.png" style="bottom: 2px"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">Sobre mim</h5>
              <div style="width: 120px;">
                <v-slider v-model="slider2" color="yellow"></v-slider>
              </div>
              <h4 class="mt-n4">Eu sou um Web Design</h4>
              <h4>e Desenvolvedor Criativo</h4>
              <p class="text-grey">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus optio
                deserunt, animi praesentium odio doloremque autem dicta accusamus doloribus quis eum sed modi fugiat
                vero iusto tenetur repellat. </p>
              <br />
              <p class="text-grey">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Necessitatibus optio
                deserunt, animi praesentium odio doloremque autem dicta accusamus doloribus quis eum sed modi fugiat
                vero iusto tenetur repellat. </p>
              <v-btn tile dark color="yellow" class="mt-4">
                Download Curriculo
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>O que nós fazemos</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor <br /> sit amet consectetur adipisicing elit. <br />Rem, aspernatur.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor <br /> sit amet consectetur adipisicing elit. <br />Rem, aspernatur.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-camera" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Fotografia</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor <br /> sit amet consectetur adipisicing elit. <br />Rem, aspernatur.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Desing</v-btn>
          <v-btn class="mr-2" variant="tonal">Fron Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card :elevation="isHoverImg ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props">
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Carregar mais</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="i10.jpg" height="200px" cover></v-img>
                <v-cart-title>Nós fornecemos a você o melhor</v-cart-title>
                <v-card-subtitle>
                  By Marcio Navarro Pro | 06 julho 2024
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis ullam cum ipsa corrupti quas
                  odit
                  fugiat in possimus.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="i11.jpg" height="200px" cover></v-img>
                <v-cart-title>Nós fornecemos a você o melhor</v-cart-title>
                <v-card-subtitle>
                  By Marcio Navarro Pro | 06 julho 2024
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis ullam cum ipsa corrupti quas
                  odit
                  fugiat in possimus.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="i12.jpg" height="200px" cover></v-img>
                <v-cart-title>Nós fornecemos a você o melhor</v-cart-title>
                <v-card-subtitle>
                  By Marcio Navarro Pro | 06 julho 2024
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis ullam cum ipsa corrupti quas
                  odit
                  fugiat in possimus.
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Contrate-me para seu projeto incrível</h1>
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt facilis explicabo sequi maxime? At,
                nulla!
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mt-15">Hire me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-container>
  </v-app>
</template>

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
        {
          img: "i3.jpg"
        },
        {
          img: "i4.jpg"
        },
        {
          img: "i5.jpg"
        },
        {
          img: "i6.jpg"
        },
        {
          img: "i7.jpg"
        },
        {
          img: "i8.jpg"
        },
        {
          img: "i9.jpg"
        }
      ]

    }
  },

  components: {
    NavBar,
  },
});
</script>

<style scoped>
.v-container {
  padding: 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}

.head::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #FBDF7E;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%
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
  background-color: #F5F5F5;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9efe9;
  margin-top: -24px;
}
</style>
