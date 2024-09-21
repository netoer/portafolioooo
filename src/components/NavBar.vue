<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
      <v-icon color="blue" left class="mr-2">fas fa-signature</v-icon>EVC
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-white">Home</v-btn>
    <v-btn text @click="scroll('about')" class="text-white">About</v-btn>
    <v-btn text @click="scroll('Portfolio')" class="text-white">Portfolio</v-btn>
    <v-btn text @click="scroll('services')" class="text-white">Services</v-btn>
    <v-btn text @click="scroll('biog')" class="text-white">Biog</v-btn>
    <v-btn text @click="scroll('blog')" class="text-white">Blog</v-btn>
    <v-btn text @click="scroll('contact')" class="text-white">Contact</v-btn>
  </v-app-bar>  
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      } else {
        console.warn(`Elemento con ID '${refName}' no encontrado.`);
      }
    }
  }
}
</script>

<style>
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
.head:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
  
}
</style>
