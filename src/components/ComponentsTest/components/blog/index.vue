<template lang="">
  <div>
    <h2>{{ post.title || "-" }}</h2>
    <p>{{ post.desc || "-" }}</p>
    <input type="text" name="" id="" :value="inputValue" @input="$emit('input', $event.target.value)" />
    <button @click="$emit('enlarge', 2)">click to create size</button>
    <br>
    <slot></slot>
  </div>
</template>
<script>
export default {
  name: "Blog",
  props: {
    post: Object,
    inputValue: String,
  },
};
</script>
<style lang=""></style>
