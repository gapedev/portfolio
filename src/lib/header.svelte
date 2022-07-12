<script>
import RedesSociales from "./redes-sociales.svelte";
import Menu from "$lib/menu.svelte";

let showModal = false;
let nombre = "Gabi Pérez";

</script>
<header class="global-container">
  <div class="header-container">
   <div class="header-logo">
    <a href="/">
      <h1>{nombre}</h1>
    </a>
   </div>
   <div class="header-curriculum">
    <button>Descargar CV</button>
   </div>
  </div>

  <Menu/>

  <RedesSociales/>

</header>

<style>
 .header-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 20px 0;
 }

  h1 {
    font-size: 1.5rem;
    font-weight: 500;
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