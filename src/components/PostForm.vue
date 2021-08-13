<template>
  <form class="createPost" @submit.prevent>
    <h4 class="createPost__header">Create post</h4>
    <my-input v-focus v-model="post.title" type="text" placeholder="Name" />
    <my-input v-model="post.body" type="text" placeholder="Description" />
    <my-button class="postBtns__btn" @click="createPost">
      Create
    </my-button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style scoped>
.createPost {
  display: flex;
  flex-direction: column;
}

.createPost__header {
  font-size: 26px;
}

.postBtns__btn {
  margin-top: 50px;
}
</style>
