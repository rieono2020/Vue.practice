<template>
  <div class="container">
    {{users}}
    {{users}}
  </div>
</template>

<script>
const axios = require('axios')
let url = 'https://jsonplaceholder.typicode.com/users'

export default {
  asyncData ({params}) {
    return axios.get(url)
      .then((res) => {
        return { users : res.data }
      })
  }
}
</script>

<style>

</style>
