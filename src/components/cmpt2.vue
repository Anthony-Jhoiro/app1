<template>
  <ul>
    <li v-for="item in listes[lid]" :key="item.id">{{ item.label }}</li>
  </ul>
  <cmpt-3 :[lst]="listes[parseInt(lid)]" direction="ASC" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import cmpt3 from "./cmpt3.vue";

export default defineComponent({
  name: "cmpt2",
  props: {
    lid: Number,
  },
  components: {
    cmpt3,
  },
  data() {
    return {
      listes: [
        [
          { id: 0, label: "l1.a" },
          { id: 1, label: "l1.b" },
          { id: 2, label: "l1.c" },
          { id: 3, label: "l1.d" },
        ],
        [
          { id: 0, label: "l2.a" },
          { id: 1, label: "l2.b" },
          { id: 2, label: "l2.c" },
          { id: 3, label: "l2.d" },
        ],
        [
          { id: 0, label: "l3.a" },
          { id: 1, label: "l3.b" },
          { id: 2, label: "l3.c" },
          { id: 3, label: "l3.d" },
        ],
      ],
    };
  },
});
</script>

<style>
</style>