<script>
import {elements} from '../services/menu'
import { page } from '$app/stores';

let current;

</script>

<nav>

   <div class="main-menu">
    <ul>
          {#each elements as {nombre, icono, ruta}}
            <li class:active={$page.url.pathname === `${ruta}`}>
            <a href={ruta}>
            <div>
              <i class={icono}></i>
            </div>
            <span>{nombre}</span>
            </a>
          </li>
          {/each}
      </ul>
   </div>

   <div class="main-menu-mobile">
    <ul>
      {#each elements as {nombre, icono, ruta}}
        <li class:active={$page.url.pathname === `${ruta}`}>
        <a href={ruta}>
        <div>
          <i class={icono}></i>
        </div>
        <span>{nombre}</span>
        </a>
      </li>
      {/each}
  </ul>
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
    background-color: var(--color-hover-main);
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

  .main-menu-mobile {
    display: none;
  }

  @media (max-width:820px) {

    .main-menu {
      display: none;
    }

    .main-menu-mobile {
      display: inherit;
      position: fixed;
      bottom: 0;
      width: 100%;
      background-color: #FFFF;
      box-shadow: 7px 7px 7px 7px rgba(255,135,99,.09);
    }

    .main-menu-mobile ul{
      display: flex;
      justify-content: space-evenly;
      list-style: none;
      width: 100%;
      padding: 10px;
    }

    .main-menu-mobile span{
      display: none;
    }

    .main-menu-mobile i{
      font-size: 30px;
      color: var(--color-main);
    }

    .main-menu-mobile ul li.active i{
     color: var(--color-hover-main);
    }
  }
</style>