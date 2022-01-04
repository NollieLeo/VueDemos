<template lang="">
  <div>
    <input v-model="checked" value="jack" type="radio" name="tom" id="jack" />
    <label for="jack">jack</label>
    <input v-model="checked" value="tom" type="radio" name="tom" id="tom" />
    <label for="tom">tom</label>
    <input
      v-model="checked"
      value="billy"
      type="radio"
      name="billy"
      id="billy"
    />
    <label for="billy">billy</label>
    <br />
    <span v-for="(item, index) in checked" :key="index">{{ item }}</span>
    <br />
    <textarea v-model="textValue" name="" id="" cols="30" rows="10"></textarea>
    <br />
    <select name="" id="" multiple v-model="selectedData">
      <option
        v-for="(item, index) in ['请选择', 1, 2, 3, 4]"
        :key="index"
        :value="index ? item : ''"
        :disabled="index === 0"
      >
        {{ item }}
      </option>
    </select>
    <p>{{ selectedData }}</p>
    <br />
    <input type="checkbox" v-model="toggle" true-value="yes" false-value="no" />
    <select v-model="selectedData2" name="" id="">
      <option :value="item" v-for="(item, index) in objectArr" :key="index">
        {{ item }}
      </option>
    </select>
    <p>{{ selectedData2 }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      checked: [],
      textValue: "",
      selectedData: [],
      toggle: "yes",
      selectedData2: [],
      objectArr: [
        {
          name: "weng",
          id: 1,
        },
        {
          name: "kai",
          id: 2,
        },
        {
          name: "min",
          id: 3,
        },
      ],
    };
  },
};
</script>
<style lang=""></style>
