<template>
  <div class="divUser">
    Nome:
    <h4>{{ post.name }}</h4>
    <br />
    Apelido:
    <h4>{{ post.username }}</h4>
    <br />
    Email:
    <h4>{{ post.email }}</h4>
    <br />
    Endereço:
    <h4>{{ post.address }}</h4>
  </div>
</template>

<script>
export default {
  name: 'UserTile',
  props: {
    post: { type: Object, required: true }
  }
}
</script>

<style></style>
