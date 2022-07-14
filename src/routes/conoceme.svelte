
<script>
import About from "$lib/about.svelte";
import Subtitle from "$lib/subtitle.svelte";
import TituloSeccion from "$lib/titulo-seccion.svelte";

</script>



<section class="container">
 <TituloSeccion titulo="Conóceme"/>
 <div class="about-container">

  <div class="about-image">
    <div>
      <img src="../perfil.jpg" alt="">
    </div>
  </div>

  <div class="about-text">
    <div class="about-subtitle">
      <Subtitle subtitulo="Front End Developer"/>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Reiciendis officiis ipsam, dicta velit beatae modi deleniti libero nostrum perspiciatis labore dignissimos voluptatibus molestias commodi ab ad vel. Aliquid, inventore obcaecati?</p>
    <div>
      <About 
      mail="gapedev@gmail.com" 
      phone="601068778" 
      adress="Palma de Mallorca"/>
    </div>
  </div>


 </div>
</section>

<style>
.about-container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  align-items: flex-start;
}
.about-container img {
  width: 100%;
  border-radius: 20px;
  margin: 0 50px;
}
.about-subtitle {
  padding: 0 50px;
  margin-bottom: 20px;
  text-align: center;
}
.about-text {
  padding: 0px 80px;
}
</style>