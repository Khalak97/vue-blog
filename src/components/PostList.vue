<template>
  <div class="postList" v-if="posts.length > 0">
    <h3 class="postList__header">List items:</h3>
    <transition-group name="post-list">
      <PostItem
        v-for:="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove', post)"
      />
    </transition-group>
  </div>
  <h3 class="postList__info" v-else>List is empty!</h3>
</template>

<script>
import PostItem from "./PostItem.vue";

export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.postList__header {
  font-size: 32px;
  font-weight: 500;
}

.postList__info {
  font-size: 32px;
}

.post-list-item {
  display: inline-block;
  margin-right: 10px;
}

.post-list-enter-active,
.post-list-leave-active {
  transition: all 0.4s ease;
}

.post-list-enter-from,
.post-list-leave-to {
  opacity: 0;
  transform: translateX(130px);
}

.post-list-move {
  transition: transform 0.4s ease;
}
</style>
