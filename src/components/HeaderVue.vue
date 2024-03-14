<template>
  <header class="app-header">
    <div v-if="text !== ''" class="logo">
      <span>{{ text }}</span>
    </div>
    <nav class="app-header-nav">
      <slot></slot>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "HeaderVue",
  props: {
    text: {
      type: String,
      require: false,
      default: "",
    },
  },
});
</script>

<style scoped>
.app-header {
  background-color: brown;
  height: 15%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  padding: 0px 40px;
}

.app-header-nav {
  background-color: blueviolet;
  height: 100%;
  width: 15%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
</style>