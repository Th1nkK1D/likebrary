<script lang="typescript">
	import Book from './Book.svelte';
	import bookData from './mockBookdata';
</script>

<main>
	<div class="header">
		<h1>LK's Library</h1>
		<p class="subtitle">Feel free to morrow one because book is meant for sharing.</p>
	</div>
	
	<div class="bookshelf">
		{#each bookData as book}
			<Book book={book} />
		{/each}
	</div>
</main>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css?family=Bai+Jamjuree|Playfair+Display:600&display=swap');
	main {
		margin: 0 auto;
		padding: 2rem 4rem;
		font-family: 'Bai Jamjuree';

		h1 {
			font-family: 'Playfair Display', 'sans-serif';
			font-size: 4rem;
			margin: 0;
		}

		.subtitle {
			font-size: 1.2rem;
		}
	}
</style>