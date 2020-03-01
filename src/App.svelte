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
	@import url('https://fonts.googleapis.com/css?family=Bai+Jamjuree:400,500|Playfair+Display:600&display=swap');

	$screen-sm-md: 800px;
	$screen-md-lg: 1200px;

	main {
		font-family: 'Bai Jamjuree';
		margin: 0 auto;
		padding: 1rem 1rem;

		@media (min-width: $screen-sm-md){
			padding: 2rem 4rem;
		}

		.header {
			margin-bottom: 2rem;

			h1 {
				font-family: 'Playfair Display', 'sans-serif';
				margin: 0;
				line-height: 1;
				font-size: 3rem;

				@media (min-width: $screen-sm-md){
					font-size: 4rem;
				}
			}

			.subtitle {
				font-size: 1.2rem;
				margin: 0.5rem 0;
			}
		}

		.bookshelf {
			display: grid;
			grid-gap: 1rem;
			grid-template-columns: repeat(1, 100%);

			@media (min-width: $screen-sm-md){
				grid-template-columns: repeat(2, 50%);
				grid-gap: 2rem;
			}

			@media (min-width: $screen-md-lg){
				grid-template-columns: repeat(3, 33%);
			}
		}
	}
</style>