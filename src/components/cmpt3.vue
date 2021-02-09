<template>
  <ul>
    <li v-for="item in filterdLst" :key="item.id">{{ item.label }}</li>
  </ul>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "cmpt3",
  props: {
    lst: { type: Array },
    direction: String,
  },
  computed: {
    filterdLst(val) {
      if (this.direction.toUpperCase() === "DESC") {
        return this.lst.reverse();
      }
      return this.lst;
    },
  },
});
</script>

<style>
</style>