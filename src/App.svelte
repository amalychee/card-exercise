<script>
	export let name;
	let visible = false;
	let src = "https://images-na.ssl-images-amazon.com/images/S/influencer-profile-image-prod/logo/influencer-aa8cfdaf_1646419621336_original._CR32,0,1196,1196_._FMjpg_.jpeg";

	function toggleVis(){
		visible = !visible;
	}
</script>

<main>
	<nav>
		<a href="">Home</a>
		<a href="">Discover</a>
		<a href="">About Us</a>
	</nav>
	<h1>Hello {name}!</h1>
	
	<section id="panko">
		<div class="card">
			{#if !visible}
				<h2>hit the button to learn more!</h2>
				<button on:click={toggleVis}>click me!</button>
			{/if}
			{#if visible}
				<h2>panko a. cat</h2>
				<h4>@fatfatpankocat</h4>
				<img src="{src}" alt="picture of panko the cat"/>
				<p>panko a. cat is a cat influencer popular on instagram for her wonderful pictures and her spectacular hula hoop tricks. she has a masters degree in cat engineering from carnegie mellon university. please follow her on instagram and twitter.</p>
				<button on:click={toggleVis}>click me to unlearn info :(</button>
			{/if}
		</div>
	</section>
	
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	nav {
		padding: 16px;
		margin: 16px;
		background-color: rgb(255, 248, 238);
	}
	
	nav a {
		color: navy;
		background-color: rgb(255, 248, 238);
		margin: 16px 0 0 16px;
	}
	
	a:hover{
		color:blueviolet;
	}
	
	img {
		max-width: 400px;
		border-radius: 16px;
		object-fit:cover;
	}
	
	#panko{
		max-width: 700px;
		margin: auto;
	}
	
	#panko div{
		height: fit-content;
		background-color: rgb(255, 248, 238);
		box-shadow: 4px 8px 16px rgb(105, 97, 87);
		padding: 16px;
		border-radius: 24px;
	}
	
	h2, h4 {
		padding: 0px;
		margin: 8px;
	}
	
	h4 {
		color: rgb(101, 81, 77);
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	button{
		background-color: rgb(236, 199, 103);
		border-color: rgb(236, 199, 103);
		color:rgb(87, 70, 50);
		border-radius: 8px;
		padding: 8px 12px 8px 12px;
	}
	
	button:hover {
		background-color: rgb(90, 82, 72);
		border-color: rgb(90, 82, 72);
		color:white;
	}
</style>