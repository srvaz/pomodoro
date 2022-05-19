<script setup>
// General Font
import "vfonts/Lato.css";
// Monospace Font
import "vfonts/FiraCode.css";
import HelloWorld from "./components/HelloWorld.vue";
import { defineComponent } from "vue";
import { darkTheme, NConfigProvider, NGlobalStyle } from "naive-ui";

defineComponent({
  components: {
    NGlobalStyle,
  },
  setup() {
    return {
      NConfigProvider,
      darkTheme,
    };
  },
});
</script>

<template>
  <n-config-provider :theme="darkTheme">
    <n-global-style />
    <main>
      <HelloWorld />
    </main>
  </n-config-provider>
</template>

<style lang="scss">
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  position: relative;
  font-weight: normal;
  font-family: "Lato", sans-serif;
}

main {
  align-items: center;
  display: flex;
  height: 100vh;
  justify-content: center;
  width: 100vw;
}
</style>
