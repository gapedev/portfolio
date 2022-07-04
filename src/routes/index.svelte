<script>

import Bucles from "../components/Bucles.svelte";
import Ejemplo from "../components/Ejemplo.svelte";
import Eventos from "../components/Eventos.svelte";
import Promesas from "../components/Promesas.svelte";

let momento = 'tarde';

</script>

<main>

  <div>
    <h1>Empezando Portfolio</h1>
    <p>Inicio de Portfolio con Svelte</p>
    <span>{momento}</span>
  </div>

  <Ejemplo nombre="Gabi" palabra="País" />

  <Eventos />

 <div>
  <Bucles />
 </div>

 <Promesas />

</main>

<style>

</style>