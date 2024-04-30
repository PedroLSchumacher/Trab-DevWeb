<template>
  <div class="divUser">
    Nome: 
    <h4> {{ post.name }}</h4>
    <br />
    Apelido:
    <h4>{{ post.username }}</h4>
    <br />
    Email:
    <h4>{{ post.email }}</h4>
    <br />
    Endereço:
    <table>
    <tr>
      
      <br>
      <tr>
        <td>Rua: {{ post.address.street }}</td>
      </tr>
      <tr>
        <td>Logradouro: {{ post.address.suite }}</td>
      </tr>
      <tr>
        <td>Cidade: {{ post.address.city }}</td>
      </tr>
      <tr>
        <td>CEP: {{ post.address.zipcode }}</td>
      </tr>
      <tr>
        <td>Latitude: {{ post.address.geo.lat }}</td>
      </tr>
      <tr>
        <td>Longitude: {{ post.address.geo.lng }}</td>
      </tr>
      <th>{{ post.street }}</th>
    </tr>
    </table>
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

<style>

.divUser {
    border: 1px solid #ccc;
    padding: 1rem;
    margin: 1rem 0;
}

table {
  border: 1px solid #ccc;
  padding: 1rem;
  margin: 1rem 0;
  
}

h4 {
  border: 1px solid #ccc;
  padding: 1rem;
  margin: 1rem 0;
  
}

</style>
