<template>
  <form @submit.prevent class="form">
    <h4>Create post</h4>
    <my-input
        v-model="post.title"
        placeholder="Title"
    />
    <my-input
        v-model="post.body"
        placeholder="Description"
    />
    <my-button
        class="form__btn"
        @click="createPost"
    >
Create
    </my-button>
  </form>
</template>

<script>
export default {
  name: "PostForm",
  data() {
    return {
      post: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post);
      this.post = {
        title: '',
        body: ''
      }
    }
  }
}

</script>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
}

.form__btn {
  margin-top: 15px;
  align-self: flex-end;
}
</style>