<script>
  
 const elements = [
  {nombre:'Inicio', icono: "fa-solid fa-house-chimney",ruta:'/'},
  {nombre:'Conóceme', icono: "fa-solid fa-address-card",ruta:'/conoceme'},
  {nombre:'Portfolio', icono: "fa-solid fa-tarp",ruta:'/portfolio'},
  {nombre:'Proyectos', icono: "fa-solid fa-diagram-project" ,ruta:'/proyectos'},
  {nombre:'Contacto', icono: "fa-solid fa-envelope" ,ruta:'/contacto'}
]

  let link = false;

   function handleClick() {
        link = !link;
    }
</script>

<nav>

   <div class="main-menu">
    {#each elements as {nombre, icono, ruta}, index}
    <ul>
      
      <li id={index} on:click={handleClick} class:active={link}>
        <a href={ruta}>
        <div>
          <i class={icono}></i>
        </div>
        <span>{nombre}</span>
        </a>
      </li>

    </ul>
    {/each}
   </div>
  
</nav> 

<style>

  .main-menu {
    position: fixed;
    top: 50%;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
    width: 100%;
    right: 0;
    padding: 0 2vw;
    max-width: 15%
  }
  
  .main-menu ul li {
    margin: 0 0 12px;
    background-color: #fff;
    position: relative;
    height: 70px;
    width: 70px;
    padding: 23px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 18px 18px 48px rgb(108 99 255 / 10%);
    transition: all .3s ease;
  }

  .main-menu ul li.active{
    background-color: var(--color-main);
  }

  .main-menu ul li.active span:hover {
    left: 2.875rem;
    color: #FFF;
  }

  .main-menu ul li.active {
    width: 160px;
  }

  .main-menu ul li:hover{
    width: 160px;
  }

  .main-menu ul li a{
    text-decoration: none;
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    top: 0;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .main-menu ul li a{
   justify-content: flex-start;
   padding-left: 22px;
  }

  .main-menu ul li:hover a span{
   color: #000;
   left: 46px;
  }

  .main-menu ul li span{
    font-size: 16px;
    color: #222;
    font-weight: 700;
    left: 100%;
    top: 50%;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
    padding-left: 12px;
    position: absolute;
    white-space: nowrap;
    text-transform: uppercase;
    transition: all .3s ease;
  }

  .main-menu ul li i{
    font-size: 25px;
    color: #ff451b;
    display: block;
    transition: all .3s ease;
  }

  .main-menu ul li.active a span{
   color: #FFFF;
   left: 46px;
  }

  .main-menu ul li.active i{
   color: #FFFF;
  }
</style>