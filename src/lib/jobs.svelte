<script>

const jobs = [
  {link:'https://w2fly.es', image:'../w2fly.png', title:'W2FLY'},
  {link:'https://w2fly.es', image:'../w2fly.png', title:'W2FLY'},
  {link:'https://w2fly.es', image:'../w2fly.png', title:'W2FLY'},
  {link:'https://w2fly.es', image:'../w2fly.png', title:'W2FLY'},
]

</script>

<div class="cards-container">
  {#each jobs as {link, image, title} }
    <a target="_blank" href={link}>
  <div class="card-container">
    <div class="card-image">
      <img src={image} alt={title}>
    </div>
    <div class="card-info">
      <h2>{title}</h2>
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores iusto numquam cum reiciendis recusandae beatae possimus aliquid ea, dolore quisquam.</p>
    </div>
  </div>
</a>
  {/each}

</div>

<style>

  .cards-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
  .card-container {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: #FFFF;
    box-shadow: 12px 7px 12px 7px rgba(255,135,99,.09);
    transition: ease-in-out 0.3s;
    border-radius: 10px;
    margin: 10px 30px;
  }

  .card-container:first-child {
    margin-top: 30px;
  }

  .card-container:hover {
    transform: scale(1.1);
    transition: ease-in-out 0.3s;
  }

  .card-image img {
    width: 100%;
  }

  .card-image img:hover {
    filter: grayscale(90%);
    
  }

</style>