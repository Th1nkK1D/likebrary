<script lang="typescript">
  interface Book {
    volumeInfo: {
      title: string,
      subtitle: string,
    },
    imageLinks: {
      thumbnail: string
    }
  }

  export let book: Book;
</script>

<div>
  <img src={book.volumeInfo.imageLinks.thumbnail} alt={book.volumeInfo.title}/>
  <h4>{book.volumeInfo.title}</h4>
  {book.volumeInfo.subtitle}
</div>
