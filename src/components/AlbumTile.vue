<template>
<div class="divAlbum">
    <h2>{{ post.title }}</h2> <br>
    Number: {{ post.id }} <br>
    User number: {{ post.userId }}
</div>
</template>


<script>
export default {
    name: 'AlbumTile',
    props: {
        post: {type: Object, required: true}
    }
}

</script>

<style>

.divAlbum {
border: 1px solid #ccc;
padding: 1rem;
margin: 1rem 0;
}

</style>
    