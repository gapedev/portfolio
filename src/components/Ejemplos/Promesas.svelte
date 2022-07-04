<script>
import Bucles from "./Ejemplos/Bucles.svelte";

  function fetch() {
    return new Promise ((resolve, reject) => {
      setTimeout(() => {
        resolve ({
          nombre: "Rita la Cantaora",
          edad: 41,
          ocupación: "Cantaora"
        })
        reject("Tenemos un problema para sacar los datos")
      }, 3000);
    })
  }
</script>

{#await fetch()}
<p>Un segundo que estamos resolviendo cosas...</p>
  
{:then payload} 
  <p>Nombre: {payload.nombre}</p>
  <p>Edad: {payload.edad}</p>
  <p>Ocupación: {payload.ocupación}</p>

  {:catch error}
  <strong>Error: {error}</strong>
{/await}