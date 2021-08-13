<template>
  <select class="selectSort" value="modelValue" @change="changeOption">
    <option disabled value="">Choose</option>
    <option v-for="option in options" :key="option.value" :value="option.value">
      {{ option.name }}
    </option>
  </select>
</template>

<script>
export default {
  name: "my-select",
  props: {
    modelValue: {
      type: String,
    },
    options: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    changeOption(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.selectSort {
  height: 44px;
  width: 200px;
  background-color: white;
  color: teal;
  font-size: 18px;
  border: 1px solid teal;
  border-radius: 5px;
}
</style>
