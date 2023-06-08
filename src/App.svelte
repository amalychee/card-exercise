<script>
	export let name;
	import Card from "./card.svelte"
</script>

<main>
	<nav>
		<a href="">Home</a>
		<a href="">Discover</a>
		<a href="">About Us</a>
	</nav>
	<section class="header">
		<h1>Hello {name}!</h1>
	</section>
	<section id="panko">
		<div>
		<Card></Card>
		</div>
	</section>
</main>

<footer>
	<p> i hope u have a great day :D </p>
</footer>

<style>
	main {
		text-align: center;
		padding: 0;	
		margin: 0 auto;
		
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	.header{
		
		display:grid;
		place-items: center;
	}

	nav {
		position: fixed;
		text-align: left;
		width: 100%;
		padding: 16px 16px 20px 24px;
		margin: 0;
		background-color: rgb(255, 248, 238);
	}
	
	nav a {
		color: navy;
		background-color: rgb(255, 248, 238);
		padding: 16px;
	}
	nav a:hover {
		background-color: rgb(236, 199, 103);
		padding: 16px;
	}
	
	a:hover{
		color:white;
	}

	#panko{
		width: 60%;
		margin: auto;
	}
	
	#panko div{
		height: fit-content;
		background-color: rgb(255, 248, 238);
		box-shadow: 4px 8px 16px rgb(105, 97, 87);
		padding: 16px;
		border-radius: 24px;
	}

	footer {
		text-align: center;
		background-color: white;
		padding: 16px 16px 32px;
		margin: 24px;
	}
	
</style>