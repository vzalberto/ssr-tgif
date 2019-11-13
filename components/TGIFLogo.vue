<template>
	<div class="box">
		<h1>{{text}}</h1>
	</div>
</template>

<script>

export default {
  name: 'TGIFLogo',
  props: {
  	text: {
    	type: String,
    	required: true
  	},
  }
}
</script>

<style>

	.box {
		display: flex;
	}

</style>
