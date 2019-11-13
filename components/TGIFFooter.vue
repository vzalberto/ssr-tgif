<template>

	<div class="box">
		<ul>
			<li><a href="https://github.com/vzalberto/ssr-tgif" target="_blank"><b>?</b></a></li>
		</ul>
	</div>

</template>

<style>

	.box {
		display: flex;
		flex-direction: row;
	}

	ul {
		list-style-type: none;
		padding: 0;
		display: flex;
	}

	a {
		display: block;
		font-size: 2em;
		text-decoration: none;
		text-align: center;
		padding: 10px;

    border:10px solid none;
    border-radius: 100px;
	}

	a:hover {
		background-color: black;
		color: white;
	}

</style>


<script>
	export default {
	  name: 'TGIFFooter',
	}
</script>