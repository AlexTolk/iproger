<template>
  <div >
    <button @click="deleteUser(index)">Delete</button>
    <h3>{{ user.name }}</h3>
    <p>{{ user.email }} -- {{ user.password }}</p>
  </div>
</template>

<script>
  export default {
    props: {
      user: {
        type: Object,
        required: true
      }
    },
    index: {
      type: Number,
      required: true
    },
    deleteUser: {
      type: Function,
      required: true
    }
  }
</script>

<style scoped>
</style>
