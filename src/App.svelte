<script lang="typescript">
	import Book from './Book.svelte';
	import bookData from './mockBookdata';
</script>

<main>
	<h1>LK's Library</h1>
	<p>Feel free to morrow one because book is meant for sharing.</p>
	<div>
		{#each bookData as book}
			<Book book={book} />
		{/each}
	</div>
</main>

<style lang="scss">
	main {
		margin: 0 auto;
		padding: 0 4rem;
	}
</style>