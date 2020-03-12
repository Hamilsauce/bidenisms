<template>
	<div id="app">
		<HelloWorld msg="Biden Insult Generator" />
		<a href="https://hamilsauce.github.io/bidenisms/images/6.jpg">
			<img
				alt="dwight"
				src="https://hamilsauce.github.io/bidenisms/images/6.jpg"
				width="100%"
			>
		</a>
		<div class="button-container">
			<button class="new-button">New Insult</button>
			<button class="share-button">Share</button>
		</div>
	</div>
</template>

<script>
	import HelloWorld from "./components/HelloWorld.vue";

	export default {
		name: "App",
		components: {
			HelloWorld
		}
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
