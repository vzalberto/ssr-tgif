
<i>[Link a TGIF! en Netlify](https://loving-beaver-048871.netlify.com/)</i>

• Así se ve `pages/index.vue`

```html
<template>
  <div class="container">
      <TGIFLogo :text="'TGIF!'" />
      <TGIF :gifs="loadedGifs" />
      <TGIFFooter />
  </div>
</template>
```

• Dentro de `<TGIFLogo /> me gustaría lograr un component basado en zfont [https://codepen.io/vzalberto/pen/gOOdvBq](https://codepen.io/vzalberto/pen/gOOdvBq)


• El arreglo de gifs se obtiene con el método de Nuxt.js, `asyncData`, y se envía como prop a `<TGIF />`.

```javascript
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
    const { res } = await axios.get(GIPHY_URL)
    return {
      loadedGifs : res.data
    }
  }
}
```
• Template de `<TGIF />` 

```html
<template>

 <div class="box">

  <div 
   class="gif"
   v-bind:key="gif.id"
   v-for="gif in gifs">

   <img 
    :src=gif.images.fixed_height.url />

   </div>	

  </div>

</template>
```

• Correr la aplicación en local con yarn:

> yarn dev


• Se genera el directorio `dist` con este comando en Netlify:

> yarn generate