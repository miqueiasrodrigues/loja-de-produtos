<template>
  <button @click="handleClick">{{ text }}</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "ButtonVue",
  props: {
    text: {
      type: String,
      require: true,
      default: "",
    },
    action: {
      type: Function,
      require: false,
      default: () => null,
    },
  },
  methods: {
    handleClick() {
      this.action();
    },
  },
});
</script>