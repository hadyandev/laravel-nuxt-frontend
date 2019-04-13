<template>
  <div class="container">
    <h2>Making API Request - The Vue Way</h2>
    <br>
    <div v-for="post in posts" :key="post.id">
      <div class="card mb-3">
        <h5 class="card-header">{{post.title}}</h5>
        <div class="card-body">
          <p class="card-text">{{post.body}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<!-- <script>
// import axios from "axios";
// export default {
//   data() {
//     return {
//       posts: []
//     };
//   },
//   mounted() {
//     axios
//       .get("https://jsonplaceholder.typicode.com/todos")
//       .then(response => {
//         console.log(response);
//         this.posts = response.data;
//       })
//       .catch(err => {
//         console.log(err);
//       });
//   }
// };
// </script> -->

<script>
import axios from "axios";
export default {
  data() {
    return { posts: "" };
  },
  async asyncData(context) {
    let { data } = await axios.get(
      "https://jsonplaceholder.typicode.com/posts"
    );
    return { posts: data };
  }
};
</script>

