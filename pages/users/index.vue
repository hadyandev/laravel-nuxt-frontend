<template>
  <div class="container">
    <h1>Nuxt User</h1>
    <p>Find User!</p>
    <input type="text" v-model="id">
    <button @click="loadUser">Load User</button>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Users"
    };
  },
  data() {
    return { id: "" };
  },
  methods: {
    loadUser() {
      this.$router.push(`/users/${this.id}`);
    }
  }
};
</script>

<style>
</style>
