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
      <div class="text-modal">
        <p>But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and will give you a complete account of the system and expound the actual teachings of the great explore</p>
      </div>
      <div class="info-modal">
        <h4>Información de Contacto</h4>
        <div class="info-modal-container">
          <a href="tel:601068778"><i class="fa-solid fa-phone"></i><span>601068778</span></a>
          <a target="_blank" href="mailto:gapedev@gmail.com"><i class="fa-solid fa-envelope"></i><span>gapedev@gmail.com</span></a>
        </div>
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
    background-image: radial-gradient(circle at 29.9% 42.68%, #51bef9 0, #3cb5f2 50%, #1daceb 100%);
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

.text-modal, .info-modal {
  padding: 1.25rem 0;
}

.info-modal h4 {
  font-weight: 500;
  font-size: 1.25rem;
}

.info-modal-container {
  display: flex;
  flex-direction: column;
  margin-top: 1rem;
}

.info-modal-container a {
  margin: 0.3125rem 0;
}

.info-modal-container span{
  font-size: 1.125rem;
  font-weight: 600;
  transition: ease-in-out 0.3s;
}

.info-modal-container span:hover{
  color: #0052CC;
  transition: ease-in-out 0.3s;
}

.info-modal-container i{
    width: 2.5rem;
    height: 2.5rem;
    line-height: 40px;
    text-align: center;
    border-radius: 50%;
    margin-right: 0.625rem;
    box-shadow: 0rem 0.625rem 0.9375rem 0rem rgb(0 0 0 / 10%);
    font-size: 1rem;
    flex: 0 0 auto;
    color: #0052CC;
}
</style>