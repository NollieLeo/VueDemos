<template lang="">
  <div id="todoLists">
    <form @submit.prevent="addNewTodo">
      <input v-model.lazy.trim="inputValue" placeholder="enter your code">
      <button>add</button>
      <button type="button" @click="todoThings = []" >clear</button>
    </form>
    <div v-if="todoThings.length">
      <div v-on:click="handleRemove(item.value, index)" v-for="(item, index) in todoThings" :key="item.id">{{index}} -- {{item.value}}</div>
    </div>
    <div v-else>No Todothings</div>
  </div>
</template>
<script>
export default {
  name: 'TodoLists',
  data () {
    return {
      todoThings: [],
      inputValue: ''
    }
  },
  methods: {
    handleRemove (value, index) {
      alert(value);
      this.todoThings.splice(index, 1)
    },
    addNewTodo () {
      const newThing = {
        value: this.inputValue,
        done: false,
        id: Math.random()
      }
      this.todoThings.push(newThing)
      this.inputValue = ''
    }
  },
}
</script>
<style scoped>
</style>