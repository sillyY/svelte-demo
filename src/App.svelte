<script>
	import Count from './components/count.svelte'
	import View from './components/view.svelte'

	let count = 0

	function onAdd() {
		count ++;
	}
	function onReduce() {
		count --;
	}
</script>

<main>
	<View number={count}/>
	<Count onAdd={onAdd} onReduce={onReduce}/>
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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>