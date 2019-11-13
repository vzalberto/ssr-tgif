<template>

	<div class="box">
		<ul>
			<li><a href="https://github.com/vzalberto/ssr-tgif" target="_blank">?</a></li>
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
		background-color: yellow;
	}

	li {
		flex-grow: 1;
		border: 1px solid blue;
	}

	a {
		display: block;
		text-decoration: none;
		text-align: center;
		padding: 10px;
	}

</style>


<script>
	export default {
	  name: 'SharingIsCaring',
	}
</script>