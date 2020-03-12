<template>
	<div id="app">
		<HelloWorld msg="Biden Insult Generator" />
		<div class="button-container">
			<button class="new-button" @click="getImage">New Insult</button>
			<button class="share-button">Share</button>
		</div>
		<a class ="imageLink" href="https://hamilsauce.github.io/bidenisms/images/6.jpg">
			<img
        class="insultImg"
				alt="dwight"
				src="https://hamilsauce.github.io/bidenisms/images/6.jpg"
				width="100%"
			>
		</a>
	</div>
</template>

<script>
	import HelloWorld from "./components/HelloWorld.vue";

	export default {
		name: "App",
		components: {
			HelloWorld
		},
		props: [],
		data() {
			return {
        images: [
          'https://hamilsauce.github.io/bidenisms/images/1.jpg',
          'https://hamilsauce.github.io/bidenisms/images/2.jpg',
          'https://hamilsauce.github.io/bidenisms/images/3.jpg',
          'https://hamilsauce.github.io/bidenisms/images/4.jpg',
          'https://hamilsauce.github.io/bidenisms/images/5.jpg',
          'https://hamilsauce.github.io/bidenisms/images/6.jpg',
        ]
      };
		},

		methods: {
      getImage() {
        const imgLink = document.querySelector('.imageLink');
        const insultImage = document.querySelector('.insultImg');
        // const newbutton = document.querySelector('.new-button');

        let i = Math.floor(Math.random() * this.images.length);

        imgLink.href = this.images[i];
        insultImage.src = this.images[i];

      }
    },
		computed: {},
		watch: {},

		/* Vue lifecycle hooks (Ref: https://vuejs.org/v2/guide/instance.html#Instance-Lifecycle-Hooks) */
		created() {},
		mounted() {},
		updated() {},
		destroyed() {}
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin: auto;
		margin-top: 60px;
		max-width: 700px;
	}
</style>
