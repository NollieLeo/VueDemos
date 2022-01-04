<template lang="">
  <div>
    <button
      @click="currentTab = item"
      :key="index"
      v-for="(item, index) in tabs"
    >
      {{ item }}
    </button>
    <component :is="currentTabComponent"></component>
  </div>
</template>
<script>
import TabA from "./components/tab-a.vue";
import TabB from "./components/tab-b.vue";
import TabC from "./components/tab-c.vue";
export default {
  name: "TabComponent",
  components: {
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      currentTab: "A",
      tabs: ["A", "B", "C"],
    };
  },
  computed: {
    currentTabComponent() {
      return `tab-${this.currentTab}`;
    },
  },
};
</script>
<style lang=""></style>
