<template>
  <div class="container">
      <TGIF :gifs="loadedGifs" />
  </div>
</template>

<script>
import axios from 'axios'
import Logo from '~/components/Logo.vue'
import TGIF from '~/components/TGIF.vue'

const GIPHY_URL = "https://api.giphy.com/v1/gifs/search?api_key=KQzPKVUFZUIpii6iYFGNphMc7ujV6UcR&q=TGIF&rating=G&limit=5"

export default {

  components: {
    Logo,
    TGIF
  },

  data () {
    return {
      loadedGifs : []
    }
  },

  async asyncData () {
    const { data } = await axios.get(GIPHY_URL)
    return {
      loadedGifs : data.data
    }
  },

}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
