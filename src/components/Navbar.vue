<template>
  <div class="navbar">
    <div class="navbar__btns">
      <my-button class="navbar__btn" @click="$router.push('/')">Main</my-button>
      <my-button class="navbar__btn" @click="$router.push('/posts')"
        >Posts by default</my-button
      >
      <my-button class="navbar__btn" @click="$router.push('/store')"
        >Posts with store</my-button
      >
      <my-button class="navbar__btn" @click="$router.push('/about')"
        >About</my-button
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.navbar {
  display: flex;
  border-bottom: 1px solid teal;
  padding-top: 20px;
  padding-bottom: 20px;
  justify-content: flex-end;
}

.navbar__btn {
  margin-left: 20px;
}
</style>
