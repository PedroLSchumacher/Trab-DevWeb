<template>
<div class="divPost">
    <h2>{{ post.title }}</h2> <br>
    <p>{{ post.url }}</p> <br>
    por: {{ post.thumbnailUrl }}
    
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

</style>
    