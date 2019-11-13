<template>
	<div class="box">
			<div class="gif" v-bind:key="gif.id" v-for="gif in gifs">
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

	.box {
		display: flex;
  		flex-wrap: wrap-reverse;
	}

	.gif {
		flex-grow: 1
	}
</style>
