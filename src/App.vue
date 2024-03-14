<template>
  <div class="app">
    <HeaderVue :text="logoName">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </HeaderVue>
    <main class="app-content">
      <router-view></router-view>
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import HeaderVue from "./components/HeaderVue.vue";
import router from "./router";

export default defineComponent({
  name: "App",
  components: {
    HeaderVue,
  },
  setup() {
    return {
      router,
      logoName: "Meu Logotipo",
    };
  },
});
</script>

<style scoped>
.app {
  height: 100%;
}
.app-content {
  background-color: blue;
  height: 85%;
  box-sizing: border-box;
  padding: 0px 40px;
}
</style>
