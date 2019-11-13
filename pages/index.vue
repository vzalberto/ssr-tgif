<template>
  <div class="container">
      <TGIFLogo :text="'TGIF!'" />
      <TGIF :gifs="loadedGifs" />
      <TGIFFooter />
  </div>
</template>

<script>
import axios from 'axios'

import TGIFLogo from '~/components/TGIFLogo.vue'
import TGIF from '~/components/TGIF.vue'
import TGIFFooter from '~/components/TGIFFooter.vue'

const GIPHY_URL = "https://api.giphy.com/v1/gifs/search?api_key=KQzPKVUFZUIpii6iYFGNphMc7ujV6UcR&q=TGIF&rating=G&limit=5"

export default {

  components: {
    TGIF,
    TGIFLogo,
    TGIFFooter,
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
  flex-direction: column;
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
