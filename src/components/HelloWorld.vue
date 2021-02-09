<template>
  <input type="text" v-model="inputValue" />
  <p v-if="cpt >= 1">{{ inputValue }}</p>
  <ul v-if="cpt >= 2">
    <li v-for="item in lst" :key="item.id">{{ item.name }}</li>
  </ul>
  <button @click="handleButton">Click me</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HelloWorld",
  props: {},

  data() {
    return {
      inputValue: "",
      cpt: 0,
      lst: [
        { id: 1, name: "name1" },
        { id: 2, name: "name2" },
        { id: 3, name: "name3" },
        { id: 4, name: "name4" },
        { id: 5, name: "name5" },
      ],
    };
  },

  methods: {
    handleButton() {
      this.cpt++;
    },
  },
});
</script>

<style scoped>
a {
  color: #42b983;
}
</style>