<script>
  function gestionarCLick() {
    console.log("CLock")
  }

  let nombre = "";

  function handle (e) {
    const target = e.target;
    nombre = e.target.value
  }
</script>


<input type="text" placeholder="Pon aquí tu nombre" class="texto" on:keyup={handle}>

{#if nombre.length === 0}

<p>No me has dicho como te llamas</p>

{:else}

<strong>Hola, {nombre}</strong>

{/if}

<button on:click={gestionarCLick}>
  Hazme Click si te atreves
</button>
