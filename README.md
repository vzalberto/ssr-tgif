
<i>[Link a TGIF! en Netlify](https://loving-beaver-048871.netlify.com/)</i>

• Me gustaría integrar un header con zfont [https://codepen.io/vzalberto/pen/gOOdvBq](https://codepen.io/vzalberto/pen/gOOdvBq)

• El arreglo de gifs se obtiene con el método de Nuxt.JS, ```asyncData```.

```javascript
  async asyncData () {
    const { data } = await axios.get(GIPHY_URL)
    return {
      loadedGifs : data.data
    }
  }
```

• El en el footer tenemos un link a este post.

• Correr la aplicación en local con yarn:

> yarn dev