<template>
  <section class="flex h-full w-screen items-center justify-center">
    <h1 class="text-[#EDEDED]">{{ translate }}</h1>
  </section>
</template>

<script>
export default {
  props: {
    translate: "",
  },
  data() {
    return {};
  },
};
</script>
