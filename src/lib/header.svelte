<script>
import RedesSociales from "./redes-sociales.svelte";
import Menu from "$lib/menu.svelte";

let nombre = "Gabi Pérez";
let curriculum = "Descargar CV"

</script>
<header>
  <div class="header-container">
   <div class="header-logo">
    <a href="/">
      <h1>{nombre}</h1>
    </a>
   </div>
   <div class="header-curriculum">
    <button>{curriculum}</button>
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
    font-weight: bold;
  }

  button {
  background-color:var(--color-main);
  border: none;
  color: white;
  font-weight: bold;
  cursor: pointer;
  padding:0.625rem;
  border-radius: 0.625rem;
  font-size: 0.875rem;
  padding: 8px 35px;
  transition: ease-in-out 0.3s;
}

button:hover {
  background-color: var(--color-hover-main);
  transition: ease-in-out 0.3s;
}
</style>