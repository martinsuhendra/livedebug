<template>
  <div id="app">
    <navigation :counter="this.favorites.length"/>
    <router-view :myFavorite="myFavorite" :favorites="favorites"/>
  </div>
</template>

<script>
import '@/assets/style.css'
import Navigation from '@/components/Navigation'

export default {
  name: 'App',
  components: {
    Navigation
  },
  data () {
    return {
      favorites: []
    }
  },
  methods: {
    myFavorite (data) {
      this.favorites = this.favorites.concat(data)
    }
  }
}
</script>

<style>
</style>
