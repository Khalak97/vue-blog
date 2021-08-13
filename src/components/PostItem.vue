<template>
  <div class="post">
    <div class="postItem">
      <div class="postItem__id">ID: {{ post.id }}</div>
      <div class="postItem__name">Name: {{ post.title }}</div>
      <div class="postItem__desc">Decription: {{ post.body }}</div>
    </div>

    <div class="postBtns">
      <my-button
        class="postBtns__btn"
        @click="$router.push(`/posts/${post.id}`)"
      >
        Open
      </my-button>
      <my-button class="postBtns__btn">
        Edit
      </my-button>
      <my-button class="postBtns__btn" @click="$emit('remove', post)">
        Delete
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
  margin-bottom: 30px;
  border: 1px solid teal;
  border-radius: 5px;
  padding: 20px 30px;
}

.postItem__id {
  font-size: 18px;
}

.postItem__name {
  font-size: 32px;
  margin-top: 5px;
  line-height: 26px;
}

.postItem__desc {
  margin-top: 15px;
  font-size: 18px;
}

.postBtns {
  display: flex;
  margin-top: 15px;
  justify-content: flex-end;
}

.postBtns__btn {
  margin-left: 20px;
}
</style>
