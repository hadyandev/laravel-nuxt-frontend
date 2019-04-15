<template>
  <div class="card bg-light mb-3" style="width: 18rem;">
    <div class="card-header">Post: {{post.id}}</div>
    <div class="card-body">
      <h5 class="card-title">
        <nuxt-link :to="{name:'posts-id', params:{id:post.id}}">{{post.title}}</nuxt-link>
      </h5>
      <nuxt-link class="btn btn-dark" :to="{name:'posts-id', params:{id:post.id}}">
        Read More
        <i class="fas fa-angle-double-right"></i>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: Object
  }
};
</script>

