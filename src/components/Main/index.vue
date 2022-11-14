<template>
  <section class="flex h-[calc(100vh-128px)] w-screen items-center flex-col">
    <h1 class="mb-2 text-[#EDEDED] 
    text-center
     text-lg w-[550px]
     pt-[60px]">{{ translate }}</h1>
     <Techs/>
  </section>
</template>

<script>
import Techs from "../Techs/index.vue";


export default {
  props: {
    translate: "",
  },
  data() {
    return {};
  },
  components: {
    Techs
  }
};
</script>
