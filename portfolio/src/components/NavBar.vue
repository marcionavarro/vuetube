<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
      <v-icon color="yellow" lef class="mr-2">fas fa-signature</v-icon>MarcioNavarro
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-yellow">Home</v-btn>
    <v-btn text @click="scroll('about')">Sobre</v-btn>
    <v-btn text @click="scroll('portfolio')">Portfólio</v-btn>
    <v-btn text @click="scroll('services')">Serviços</v-btn>
    <v-btn text @click="scroll('page')">Página</v-btn>
    <v-btn text @click="scroll('blob')">Blog</v-btn>
    <v-btn text @click="scroll('contact')">Contato</v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName)
      element.scrollIntoView({behavior: 'smooth'})
    }
  }
}
</script>

<style>
</style>