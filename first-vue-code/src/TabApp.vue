<template>
  <button @click="activetab = 'TabA'">Tab A</button>
  <button @click="activetab = 'TabB'">Tab B</button>
  <button @click="activetab = 'TabC'">Tab C</button>
  <!-- <TabA v-if="activetab === 'TabA'" />
  <TabB v-if="activetab === 'TabB'" />
  <TabC v-if="activetab === 'TabC'" /> -->
  <keep-alive>
    <component :is="activetab" />
  </keep-alive>
</template>

<script>
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";
export default {
  name: "App",
  components: {
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      activetab: "TabA",
    };
  },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
