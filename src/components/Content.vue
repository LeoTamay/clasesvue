<template>
  <div>
  <h1>{{movieTitle}}</h1>
  <table class="table">
  <thead>
  </thead>
  <tbody>
    <tr v-for="movie in movies" :key="movie.id">
      <th scope="row">{{movie.id}}</th>
      <td>{{movie.name}}</td>
      <td>{{movie.year}}</td>
      <td>{{movie.age}}</td>
    </tr>
  </tbody>
</table>
</div>
</template>

<script>
export default {
name: 'Content',
props: ['movieTitle'],
   data() {
    return {
      movies: []
    }
  },
  mounted() {
    this.loadCatalog()
  },
  methods: {
    loadCatalog: async function() {
      const data = await fetch('./catalog.json')
      this.movies = await data.json()
    }
  }
}
</script>