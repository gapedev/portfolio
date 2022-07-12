
<section class="redes-sociales-container">

    <ul>
      <li>
        <a target="_blank" href="https://github.com/gapedev"><i class="fa-brands fa-github"></i></a>
      </li>
      <li>
        <a target="_blank" href="https://www.linkedin.com/in/gabriel-p%C3%A9rez-licer%C3%A1n-b0826a14b/"><i class="fa-brands fa-linkedin-in"></i></a>
      </li>
    </ul>

</section>

<style>

.redes-sociales-container {
    position: fixed;
    top: 50%;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
    left: 0;
    width: 100%;
    max-width: 15%;
    padding: 0 2vw;
    display: flex;
    justify-content: flex-end;
  }

  .redes-sociales-container ul{
    margin: 0;
    list-style: none;
  }

  .redes-sociales-container ul li{
    margin: 0 0 12px; 
  }

.redes-sociales-container a{
    display: inline-block;
    margin-right: 10px;
    width: 50px;
    height: 50px;
    line-height: 62px;
    background-color: #ffffff;
    text-align: center;
    border-radius: 50%;
    color: var(--color-main);
    transition: ease-in-out 0.2s;
    box-shadow: 18px 18px 48px rgb(108 99 255 / 10%);
   
}

.redes-sociales-container a:hover {
    color: #fff;
    background-color: var(--color-hover-main);
    transition: ease-in-out 0.2s;
}

.redes-sociales-container a i {
   transition: 0.3s;
   font-size: 30px;
}

.redes-sociales-container a:hover i {
  transform: rotate(360deg);
}

</style>