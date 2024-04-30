<template>
    <div class="divPost">
        <h2>{{ post.title }}</h2>> <br>
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

    </style>
    