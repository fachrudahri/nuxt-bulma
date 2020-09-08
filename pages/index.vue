<template>
<div class="container">
  <Navbar/>
  <div class="columns is-multiline mt-5">
    <DataCard v-for="(item, i) in items" :key="i"
    :name="item.name"
    :username="item.username"
    :email="item.email"
    :phone="item.phone"
    :website="item.website"
    />
  </div>
</div>
</template>

<script>
import Navbar from '~/components/Navbar'
import DataCard from '~/components/DataCard'
import axios from 'axios'
export default {
  components: {
    Navbar,
    DataCard
  },
  data() {
    return {
      items: []
    }
  },
  async mounted() {
    const app = this
    await axios.get('https://jsonplaceholder.typicode.com/users')
    .then(res => {
      app.items = res.data
    }).catch(err => console.log(err))
  }
}
</script>

<style>

</style>
