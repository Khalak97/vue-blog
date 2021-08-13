<template>
  <div class="navbar">
    <div class="navbar__btns">
      <my-button @click="$router.push('/')">Main</my-button>
      <my-button @click="$router.push('/posts')">Posts by default</my-button>
      <my-button @click="$router.push('/store')">Posts with store</my-button>
      <my-button @click="$router.push('/about')">About</my-button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.navbar {
  display: flex;
}
</style>
