<script>
import Modal from "./modal.svelte";
import RedesSociales from "./redes-sociales.svelte";

let showModal = false;
let nombre = "Gabi Pérez";

</script>
<header>
  <div>
    <a href="/">
      <h1>{nombre}</h1>
    </a>
  </div>
  <nav>
    <ul>
      <li class="header-link">
        <a href="/">Home</a>
      </li>
      <li class="header-link">
        <a href="/conoceme">Conóceme</a>
      </li>
      <li class="header-link">
        <a href="/portfolio">Portfolio</a>
      </li>
      <li class="header-link">
        <a href="/proyectos">Proyectos</a>
      </li>
      <li>
        <button on:click="{() => showModal = true}">
          ¿Hablamos?
        </button>
      </li>
    </ul>
  </nav>

  {#if showModal}
	<Modal on:close="{() => showModal = false}">
		
    <section class="section-modal-container">
      <div class="header-modal">
        <h2>{nombre}</h2>
      </div>
    </section>

    <section>
      <RedesSociales/>
    </section>

	</Modal>
{/if}
</header>

<style>
  header {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 1.4375rem 0 0 0;
  }

  h1 {
    font-size: 1.5rem;
    font-weight: 500;
  }

  ul {
    display: flex;
    align-items: center;
  }

  li {
    list-style: none;
    margin-right: 1.25rem;
    font-weight: bold;
    transition: 0.3s;
    letter-spacing: 0.0688rem;
  }

  li:hover {
    color: #0052CC;
    transition: 0.3s;
  }
  button {
  background-color:#0052CC;
  border: none;
  color: white;
  font-weight: bold;
  cursor: pointer;
  padding:0.625rem;
  border-radius: 0.625rem;
}
</style>