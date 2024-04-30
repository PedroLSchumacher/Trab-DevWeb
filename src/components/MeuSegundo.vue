<template>
<div>
    {{ msg }}
    <div class="btn-list">
      <button class="btn" @click="carregarPosts()">Carregar Posts</button>
      <button class="btn" @click="carregarPhotos()">Carregar Fotos</button>
      <button class="btn" @click="carregarAlbums()">Carregar Álbuns</button>
      <button class="btn" @click="carregarComments()">Carregar Comentários</button>
      <button class="btn" @click="carregarUsers()">Carregar Usuários</button>
    </div>

    <button class="clear" @click="limparArrays()">Limpar</button>
    
    
    <p v-for="element in postArray" v-bind:key="element">
        <PostTile :post="element"/>
    </p>

    <p v-for="element in photoArray" v:bind:key="element">
        <PhotoTile :post="element"/>
    </p>

    <p v-for="element in albumArray" v:bind:key="element">
        <AlbumTile :post="element"/>
    </p>

    <p v-for="element in commentArray" v:bind:key="element">
        <CommentTile :post="element"/>
    </p>

    <p v-for="element in userArray" v:bind:key="element">
        <UserTile :post="element"/>
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
            postArray: [],
            photoArray: []
        }
    },
    created() {   
    },
    
    methods: {
        carregarPosts() {
            fetch('https://jsonplaceholder.typicode.com/posts')
        .then(response => response.json())
        .then(data => {
            this.msg = "Carregando os Posts";
            setTimeout ( () => {
                this.postArray = data;
                this.msg = "Posts carregados com Sucesso!";
            }, 2000);
        })
        },

        carregarPhotos() {
            fetch('https://jsonplaceholder.typicode.com/photos')
        .then(response => response.json())
        .then(data => {
            this.msg = "Carregando as Fotos";
            setTimeout ( () => {
                this.photoArray = data;
                this.msg = "Fotos carregadas com Sucesso!";
            }, 2000);
        })
        },
    
        carregarAlbums() {
            fetch('https://jsonplaceholder.typicode.com/albums')
        .then(response => response.json())
        .then(data => {
            this.msg = "Carregando os Álbuns";
            setTimeout ( () => {
                this.albumArray = data;
                this.msg = "Álbuns carregados com Sucesso!";
            }, 2000);
        })
        },

        carregarComments() {
            fetch('https://jsonplaceholder.typicode.com/comments')
        .then(response => response.json())
        .then(data => {
            this.msg = "Carregando os Comentários";
            setTimeout ( () => {
                this.commentArray = data;
                this.msg = "Comentários carregados com Sucesso!";
            }, 2000);
        })
        },

        carregarUsers() {
            fetch('https://jsonplaceholder.typicode.com/users')
        .then(response => response.json())
        .then(data => {
            this.msg = "Carregando os Usuários";
            setTimeout ( () => {
                this.userArray = data;
                this.msg = "Usuários carregados com Sucesso!";
            }, 2000);
        })
        },
        limparArrays(){
            this.postArray = [];
            this.photoArray = [];
            this.albumArray = [];
            this.commentArray = [];
            this.userArray = [];
        }
        }
}

</script>

<style>
.btn-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.btn {
  background-color: #a3a3a3;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

.btn:hover {
  background-color: #ddd;
}

.clear {
  margin-top: 10px;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  background-color: #ff7f7f;
}

.clear:hover {
  background-color: #ffaaaa; 
}
</style>

