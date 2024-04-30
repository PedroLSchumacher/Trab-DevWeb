<template>
<div class="divPhoto">
    <h2>{{ post.title }}</h2>
    </br>
    <img class="img" :src="post.url" alt="Imagem Principal"> 
    </br>
    <img :src="post.thumbnailUrl" alt="Miniatura"> 
</div>
</template>


<script>
export default {
    name: 'PhotoTile',
    props: {
        post: {type: Object, required: true}
    }
}

</script>

<style>

.divPhoto {
border: 1px solid #ccc;
padding: 1rem;
margin: 1rem 0;
}

</style>
    