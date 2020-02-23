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

<div class="book"> 
  <div>
    <img src={book.volumeInfo.imageLinks.thumbnail} alt={book.volumeInfo.title}/>
  </div>
  <div class="content">
    <h3>{book.volumeInfo.title}</h3>
    <p>{book.volumeInfo.subtitle}</p>
  </div>
</div>

<style lang="scss">
  .book {
    display: flex;
    flex-direction: row;
    margin: 1.5rem 0;
    width: calc(33% - 2rem);
    cursor: pointer;

    img {
      width: 120px;
      height: 100%;
      object-fit: cover;
      border-radius: 5px;
      transition: transform .25s;
    }

    .content {
      flex: 1;
      padding-left: 1rem;

      p {
        opacity: 0.6;
      }
    }

    &:hover {
      img {
        transform: translateY(-0.5rem);
      }
    }
  }
</style>