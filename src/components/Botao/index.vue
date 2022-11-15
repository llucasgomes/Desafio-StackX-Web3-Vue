<template>
  <button
    class="flex h-12 w-32 items-center justify-center gap-3 rounded-lg bg-[#27272A] font-['Inter'] font-semibold text-[#EDEDED]"
    v-on:click="handler(language)"
  >
    <img class="h-6 w-6" :src="idioma.flag" :alt="name" />
    {{ language }}
  </button>
</template>

<script>
export default {
  props: {
    idioma: {},
  },
  data() {
    return {
      language: this.idioma.idioma,
      flag: this.idioma.flag,
      name: this.idioma.name,
    };
  },
  methods: {
    handler(language) {
      // console.log(language);
      this.$emit("tradutor", language);
    },
  },
};
</script>
