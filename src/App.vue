<template>
  <div class="container">
    <post-form
        @create="createPost"
    />
    <post-list
        :posts="posts"
    />

  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  name: "App",
  components: {
    PostList,
    PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Javascript 1', body: 'Description 1'},
        {id: 2, title: 'Javascript 2', body: 'Description 2'},
        {id: 3, title: 'Javascript 3', body: 'Description 3'},
      ]
    }
  },
  methods: {
    createPost(post) {
     this.posts.push(post)
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 15px;
}

</style>