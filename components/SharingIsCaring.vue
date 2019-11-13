<template>

	<div class="box">
		<ul>
			<li><a href="#">w</a></li>
			<li><a href="#">t</a></li>
			<li><a href="#">f</a></li>
			<li><a href="#">?</a></li>
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