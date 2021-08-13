<template>
  <div class="search__input">
    <input :value="modelValue" @input="updateInput" class="input" type="text" />
  </div>
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.search__input {
  margin-top: 20px;
  margin-bottom: 20px;
  display: flex;
  border: 1px solid teal;
  height: 30px;
  border-radius: 999px;
  padding: 10px 20px;
}

.search__input > input:focus {
  outline: 0;
}

.input {
  flex: 1;
  padding: 10px 20px;
  font-size: medium;
  border: none;
}
</style>
