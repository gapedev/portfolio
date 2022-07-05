<script>
import Modal from "./modal.svelte";

let showModal = false;

</script>
<header>
  <div>
    <a href="/">
      <h1>Gabi Pérez</h1>
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
      <li class="header-link">
        <a href="/contacto">Contacto</a>
      </li>
      <li>
        <button on:click="{() => showModal = true}">
          show modal
        </button>
      </li>
    </ul>
  </nav>

  {#if showModal}
	<Modal on:close="{() => showModal = false}">
		
    <section>
      <div class="header-modal">
        <h2>Gabi</h2>
      </div>
    </section>

	</Modal>
{/if}


</header>

<style>
  header {
    display: flex;
    justify-content: space-around;
    padding: 1.4375rem 0 0 0;
  }

  h1 {
    font-size: 1.5rem;
    font-weight: 500;
  }

  ul {
    display: flex;
  }

  li {
    list-style: none;
    margin-right: 1.25rem;
    font-weight: bold;
    transition: 0.3s;
    letter-spacing: 1.1px;
  }

  li:hover {
    color: #0052CC;
    transition: 0.3s;
  }

/*   .header-link {
    display: inline-block;
}

  .header-link::after {
    content: '';
    display: block;
    width: 0;
    height: 3px;
    background: #0052CC;
    transition: width .3s;
}

  .header-link:hover::after {
    width: 100%;
} */

button {
  padding: 30px;
}

.header-modal {
  display: flex;
  justify-content: space-around;
}

</style>