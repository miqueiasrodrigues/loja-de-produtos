<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <ButtonVue :text="btnText" :action="teste"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ButtonVue from "../components/ButtonVue.vue";

export default defineComponent({
  data() {
    return {
      message: "Hello, World!",
      btnText: "teste",
    };
  },
  components:{
    ButtonVue
  },
  methods: {
    changeMessage() {
      this.message = "New message!";
    },
    btnAction() {
      this.changeMessage(); 
    },
  },
});
</script>