<template>
  <div class="post">
    <div>
      <div>{{ post.id }}</div>
      <div>Name: {{ post.title }}</div>
      <div>Decription: {{ post.body }}</div>
    </div>

    <div class="postBtns">
      <my-button @click="$emit('remove', post)">
        Delete
      </my-button>
      <my-button>
        Edit
      </my-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  padding: 15px;
  margin-top: 20px;
  border: 1px solid black;
}
</style>
