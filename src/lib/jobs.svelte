<script>
import {jobs} from "../services/jobs";
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
    grid-template-columns: repeat(auto-fill,minmax(min(100%, 300px), 1fr));
    gap: 2rem;
  }

  .card-container {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: #FFFF;
    box-shadow: 0 0 1.5625rem rgb(0 0 0 / 34%);
    transition: ease-in-out 0.3s;
    border-radius: 0.625rem;
    margin: 0.625rem 1.875rem;
    width: 280px;
  }

  .card-container:hover {
    box-shadow: 0 0 1.5625rem rgb(0 0 0 / 34%);
  }

  @media (max-width:876px) {
    .card-container {
      width: 90%;
      padding: 15px;
    }

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

  .card-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 30px;
  }

</style>