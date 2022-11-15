<template>
  <footer class="flex h-16 w-screen items-center justify-center bg-white">
    <Botao
      :v-for="(item, index) in language"
      :idioma="item"
      @click="$emit('handler')"
    />
    <p>{{ item }}</p>
  </footer>
</template>

<script>
//Imports
import Botao from "../Botao/index.vue";

export default {
  props: {
    language: {},
  },
  components: {
    Botao,
  },
};
</script>
