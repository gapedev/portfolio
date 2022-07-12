

<nav>

   <div class="main-menu">
    <ul>
      <li class="">
        <a href="/">
        <div>
          <i class="fa-solid fa-house-chimney"></i>
        </div>
        <span>Inicio</span>
        </a>
      </li>
      <li class="active">
        <a href="/conoceme"> 
        <div>
          <i class="fa-solid fa-address-card"></i>
        </div>
        <span>Conóceme</span>
      </a>
      </li>
      <li class="active">
        <a href="/portfolio">
          <div>
          <i class="fa-solid fa-tarp"></i>
        </div>
        <span>Portfolio</span>
      </a>
      </li>
      <li class="active">
        <a href="/proyectos">
          <div>
          <i class="fa-solid fa-diagram-project"></i>
        </div>
        <span>Proyectos</span>
      </a>
      </li>
      <li class="active">
        <a href="/contacto">
          <div>
            <i class="fa-solid fa-envelope"></i>
          </div>
          <span>Contacto</span>
        </a>
      </li>
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
    background-color: var(--color-main);
  }

  .main-menu ul li.active span:hover {
    left: 2.875rem;
    color: #FFF;
  }

  .main-menu ul li.active:first-child {
    width: 130px;
  }

  .main-menu ul li.active:nth-child(2) {
    width: 160px;
  }

  .main-menu ul li.active:nth-child(3) {
    width: 160px;
  }

  .main-menu ul li.active:nth-child(4) {
    width: 160px;
  }

  .main-menu ul li.active:nth-child(5) {
    width: 160px;
  }
  

  .main-menu ul li:hover:first-child{
    width: 130px;
  }

  .main-menu ul li:hover:nth-child(2){
    width: 160px;
  }

  .main-menu ul li:hover:nth-child(3){
    width: 160px;
  }

  .main-menu ul li:hover:nth-child(4){
    width: 160px;
  }

  .main-menu ul li:hover:nth-child(5){
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