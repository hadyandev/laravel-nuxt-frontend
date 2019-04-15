<template>
  <div class="container">
    <div class="card bg-light mb-3">
      <div class="card-header">Post: {{post.id}}</div>
      <div class="card-body">
        <h5 class="card-title">{{post.title}}</h5>
        <p class="card-text">{{post.body}}</p>
        <nuxt-link class="btn btn-dark" to="/posts">
          <i class="fas fa-angle-double-left"></i> Back
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { post: "" };
  },
  async asyncData({ params }) {
    let { data } = await axios.get(
      `https://jsonplaceholder.typicode.com/posts/${params.id}`
    );
    return { post: data };
  },
  head() {
    return {
      title: this.post.title
    };
  }
};
</script>