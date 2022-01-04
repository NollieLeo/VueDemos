<template lang="">
  <div :style="{ fontSize: fonsize + 'px' }">
    <Blog
      v-for="post in postsData"
      :post="post"
      :key="post.title"
      @enlarge="fonsize += $event"
      v-model="inputValue"
    >test slot</Blog>
    <span>{{ inputValue }}</span>
  </div>
</template>
<script>
import Blog from "./components/blog";
export default {
  data() {
    return {
      fonsize: 12,
      inputValue: "",
      postsData: [
        {
          title: "weng is good",
          desc: "weng is fucking good",
        },
        {
          title: "kaimin is good",
          desc: "kaimin is fucking good",
        },
        {
          title: "wengkaimin is good",
          desc: "wengkaimin is fucking good",
        },
      ],
    };
  },
  components: {
    Blog,
  },
};
</script>
<style lang=""></style>
