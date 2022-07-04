
<script>
import Tarea from "../components/Tarea.svelte"


let elementos = [
  { id:'324684616', nombre: "Comprar patatas", terminado: false},
  { id: '1549816164', nombre:"Limpiar el jardín", terminado: true},
  { id: '130561035', nombre:"Enviar correo", terminado: false},
  { id: '216546131', nombre:"Llamar a Lucía", terminado: true},
];

</script>

{#each elementos as elemento, number (elemento.id)}
 <Tarea nombre= {elemento.nombre} terminado={elemento.terminado} />

 {:else}

 <p>NO tienes nada que hacer hoy, disfruta</p>

{/each}