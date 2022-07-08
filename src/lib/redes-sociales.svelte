<script>
</script>


<section class="redes-sociales-container">
  <div class="redes-sociales-icon">
    <a href="https://github.com/gapedev"></a>
  </div>
  <div class="redes-sociales-icon">
    <a href=""></a>
  </div>
  <div class="redes-sociales-icon">
   <a href=""></a>
  </div>

  <i></i>
</section>

<style>

.redes-sociales-container {
    display: flex;
  }

.redes-sociales-icon a{
    display: flex;
    margin-right: 10px;
    width: 35px;
    height: 35px;
    line-height: 35px;
    background-color: #e7e7e7;
    text-align: center;
    border-radius: 7px;
    color: #415674
}

.redes-sociales-icon a:hover {
  color: #0052CC;
  transition: all 3s;
  -webkit-animation: rotate-center 0.6s ease-in-out both;
	        animation: rotate-center 0.6s ease-in-out both;
}

 @-webkit-keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
            transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
  }
}
@keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
            transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
  }
}

</style>