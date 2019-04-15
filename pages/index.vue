<template>
  <div class="container">
    <h1>Hello World!</h1>
    <no-ssr>
      <v-select v-model="selected" :options="['Vue.js','React']" class="form-control"></v-select>
    </no-ssr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: ""
    };
  }
};
</script>

<style>
</style>
