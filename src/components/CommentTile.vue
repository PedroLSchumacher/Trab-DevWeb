<template>
<div class="divComment">
    <h2>{{ post.name }}</h2> <br>
    <h3>{{ post.email }}</h3> <br>
    <p>{{ post.body }}</p> <br>
    Number: {{ post.id }} <br>
    Post number: {{ post.postId }}
</div>
</template>


<script>
export default {
    name: 'CommentTile',
    props: {
        post: {type: Object, required: true}
    }
}

</script>

<style>

.divComment {
border: 1px solid #ccc;
padding: 1rem;
margin: 1rem 0;
}

</style>
    