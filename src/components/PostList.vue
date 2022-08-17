<template>
  <div>
<h3>Users list</h3>
  </div>
<post-item
    v-for="post in posts"
    :post="post"
/>
</template>

<script>
import PostItem from "./PostItem.vue";

export default {
  name: "PostList",
  components: {PostItem},
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>


</style>