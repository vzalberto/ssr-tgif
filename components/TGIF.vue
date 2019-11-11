<template>
	<div>
			<div v-bind:key="gif.id" v-for="gif in gifs">
				<img :src=gif.images.fixed_height.url />
			</div>
			
	</div>
</template>

<script>
export default {
  name: 'TGIF',
  props: {
  	gifs: {
    	type: Array,
    	required: true
  	},
  }
}
</script>

<style>
	img { cursor: pointer; }
</style>
