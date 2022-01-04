<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <!-- todolists -->
    <h2>todolists</h2>
    <TodoLists></TodoLists>
    <!-- form -->
    <Form></Form>
    <!-- ComponentsTest -->
    <ComponentsTest></ComponentsTest>
    <!-- Tabs -->
    <Tabs></Tabs>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TodoLists from "./components/TodoLists.vue";
import Form from "./components/FormTest.vue";
import ComponentsTest from "./components/ComponentsTest";
import Tabs from "./components/TabComponents";

export default {
  name: "App",
  components: {
    HelloWorld,
    TodoLists,
    Form,
    ComponentsTest,
    Tabs,
  },
};
</script>

<style></style>
