<template>
  <input type="text" v-model="txt" />
  <p>Message : {{ txt }}</p>

  <cmpt-2 :lid="txt" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import cmpt2 from "./cmpt2.vue";

export default defineComponent({
  components: {
    cmpt2,
  },
  name: "cmpt1",
  data() {
    return {
      txt: "",
    };
  },
});
</script>

<style>
</style>