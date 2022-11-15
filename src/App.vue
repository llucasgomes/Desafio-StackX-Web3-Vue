<template>
  <div class="h-screen">
    <Header />
    <Main
      :translate="selected == '' ? this.flags[0].translations : selected"
      v-on:handler="handleClick"
    />
    

    <footer
      class="gap-[50px] flex h-16 w-screen items-center justify-center"
    >
      <Botao v-for="item in flags" :idioma="item" @tradutor="handleClick" />
      <p>{{ item }}</p>
    </footer>
  </div>
</template>

<script>
//Imports
import Header from "./components/Header/index.vue";
import Footer from "./components/Footer/index.vue";
import Main from "./components/Main/index.vue";
import Botao from "./components/Botao/index.vue";




export default {
  data() {
    return {
      flags: [
        {
          name: "Brasil",
          idioma: "Brasil",
          flag: "https://raw.githubusercontent.com/llucasgomes/Desafio-StackX-Web3-Vue/main/src/assets/images/flag-brazil.png",
          translations:
            "Olá, meu nome é Lucas Gomes e eu sou Desenvolvedor Front-End, Tecnologias que tenho experiência:",
        },
        {
          name: "Espanha",
          idioma: "Espanhol",
          flag: "https://raw.githubusercontent.com/llucasgomes/Desafio-StackX-Web3-Vue/main/src/assets/images/flag-spain.png",
          translations:
            "Hola, mi nombre es Lucas Gomes y soy Desarrollador Front-End, Tecnologías en las que tengo experiencia:",
        },
        {
          name: "Estados Unidos",
          idioma: "Inglês",
          flag: "https://raw.githubusercontent.com/llucasgomes/Desafio-StackX-Web3-Vue/main/src/assets/images/flag-united-states.png",
          translations:
            "Hello, my name is Lucas Gomes and I am a Front-End Developer, Technologies that I have experience:",
        },
      ],
      selected: "",
    };
  },

  components: {
    Header,
    Main,
    Footer,
    Botao,
    
  },

  methods: {
    handleClick(language) {
      console.log(language);

      if (language == "Brasil") {
        this.selected = this.flags[0].translations;
      } else if (language == "Espanhol") {
        this.selected = this.flags[1].translations;
      } else {
        this.selected = this.flags[2].translations;
      }
    },
  },
};
</script>

<style></style>
