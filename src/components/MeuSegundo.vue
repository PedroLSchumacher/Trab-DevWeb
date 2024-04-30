<template>
<div>
    {{ msg }}
    <button @click="meuArray = []">Limpar</button>
    <td><button @click="carregarPosts()">Carregar Posts</button> </td>
    <td><button @click="carregarPhotos()">Carregar Fotos</button></td>
    <td><button @click="carregarAlbums()">Carregar Albums</button></td>
    <td><button @click="carregarComements()">Carregar Comentários</button></td>
    <td><button @click="carregarUsers()">Carregar Usuários</button></td>
    
    <p v-for="element in meuArray" v-bind:key="element">
        <PostTile :post="element"/>
    </p>
</div>
</template>



<script>
//import MyHome from './MyHome.vue';
import PostTile from './PostTile.vue';
import PhotoTile from './PhotoTile.vue';
import AlbumTile from './AlbumTile.vue';
import CommentTile from './CommentTile.vue';
import UserTile from './UserTile.vue';
export default {
    name: 'MeuSegundo',
    components:{
        PostTile,
        PhotoTile,
        AlbumTile,
        CommentTile,
        UserTile
    },
    data() {
        return {
            msg: "",
            meuArray: []
        }
    },
    created() {   
    },
    
    methods: {
        carregarPosts() {
            fetch('https://jsonplaceholder.typicode.com/posts')
        .then(response => response.json())
        .then(data => {
            this.msg = "Chegou os Posts";
            setTimeout ( () => {
                this.meuArray = data;
                this.msg = "Renderizou os Posts";
            }, 2000);
        })
        },

        carregarPhotos() {
            fetch('https://jsonplaceholder.typicode.com/photos')
        .then(response => response.json())
        .then(data => {
            this.msg = "Chegou as Fotos";
            setTimeout ( () => {
                this.meuArray = data;
                this.msg = "Renderizou as Fotos";
            }, 2000);
        })
        },
    
        carregarAlbums() {
            fetch('https://jsonplaceholder.typicode.com/albums')
        .then(response => response.json())
        .then(data => {
            this.msg = "Chegou os Álbuns";
            setTimeout ( () => {
                this.meuArray = data;
                this.msg = "Renderizou os Álbuns";
            }, 2000);
        })
        },

        carregarComements() {
            fetch('https://jsonplaceholder.typicode.com/comments')
        .then(response => response.json())
        .then(data => {
            this.msg = "Chegou os Comentários";
            setTimeout ( () => {
                this.meuArray = data;
                this.msg = "Renderizou os Comentários";
            }, 2000);
        })
        },

        carregarUsers() {
            fetch('https://jsonplaceholder.typicode.com/users')
        .then(response => response.json())
        .then(data => {
            this.msg = "Chegou os Usuários";
            setTimeout ( () => {
                this.meuArray = data;
                this.msg = "Renderizou os Usuários";
            }, 2000);
        })
        }
        }
}

</script>