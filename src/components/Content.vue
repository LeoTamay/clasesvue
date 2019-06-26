<template>
  <h1>{{movieTitle}}</h1>
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
}
</script>