<template>
<button class="btn">
  <slot></slot>
</button>
</template>

<script>
export default {
  name: "my-button"
}
</script>

<style scoped>

.btn {
  padding: 10px 5px;
  color: teal;
  background: none;
  border: 1px solid teal;
  border-radius: 4px;
  text-transform: uppercase;
  min-width: 100px;
  transition: 0.3s ease-in-out;
}

.btn:hover {
  color: #fff;
  background-color: teal;
  cursor: pointer;
}
</style>