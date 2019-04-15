<template>
  <div class="container">
    <h1>Nuxt User</h1>
    <form>
      <div class="form-group">
        <label for="findUser">Find User</label>
        <input
          type="text"
          class="form-control"
          id="findUser"
          placeholder="Find User"
          v-model="id"
          required
        >
      </div>
      <button type="submit" class="btn btn-primary" @click="loadUser">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return { id: "" };
  },
  methods: {
    loadUser() {
      this.$router.push(`/users/${this.id}`);
    }
  },
  head() {
    return {
      title: "Nuxt Users"
    };
  }
};
</script>

<style>
</style>
