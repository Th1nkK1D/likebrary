<script lang="typescript">
	import Book from './Book.svelte';
	import bookData from './mockBookdata';
</script>

<main>
	<div class="header">
		<h1>LK's Bookshelf</h1>
		<p class="subtitle">Feel free to borrow some, because books is meant for sharing.</p>
	</div>
	
	<div class="bookshelf">
		{#each [...bookData, ...bookData, ...bookData] as book}
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

		.header {
			margin-bottom: 2rem;

			h1 {
				font-family: 'Playfair Display', 'sans-serif';
				font-size: 4rem;
				margin: 0;
			}

			.subtitle {
				font-size: 1.2rem;
				margin: 0.5rem 0;
			}
		}

		.bookshelf {
			display: flex;
			flex-direction: row;
			flex-wrap: wrap;
			justify-content: space-between;
		}
	}
</style>