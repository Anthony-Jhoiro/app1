<template>
  <input type="text" v-model="inputValue" />
  <p>{{ inputValue }}</p>
  <ul>
    <li v-for="item in lst" :key="item.id">{{ item.name }}</li>
  </ul>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "HelloWorld",
  props: {},

  data: () => {
    return {
      inputValue: "",
      lst: [
        { id: 1, name: "name1" },
        { id: 2, name: "name2" },
        { id: 3, name: "name3" },
        { id: 4, name: "name4" },
        { id: 5, name: "name5" },
      ],
    };
  },
});
</script>

<style scoped>
a {
  color: #42b983;
}
</style>