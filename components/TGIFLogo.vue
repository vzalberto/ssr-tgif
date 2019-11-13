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

  h1 {
    padding: 10px;
  }

  h1:hover {
    cursor: pointer;
    border:10px solid none;
    border-radius: 100px;
    background-color: black;
    color: white;
    box-shadow: 10px 10px #aaa;
  }

</style>
