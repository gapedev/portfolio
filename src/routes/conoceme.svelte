
<script>
import About from "$lib/about.svelte";
import Subtitle from "$lib/subtitle.svelte";
import TituloSeccion from "$lib/titulo-seccion.svelte";

</script>



<section class="container">
 <TituloSeccion titulo="Conóceme"/>
 <div class="about-container">

    <div class="about-image">
    </div>
    <div class="about-text">
      <div class="about-subtitle">
        <Subtitle subtitulo="Front End Developer"/>
      </div>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Reiciendis officiis ipsam, dicta velit beatae modi deleniti libero nostrum perspiciatis labore dignissimos voluptatibus molestias commodi ab ad vel. Aliquid, inventore obcaecati?</p>

        <About/>
    </div>
 </div>

</section>

<style>
.about-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  position: relative;
}
.about-image {
  background-image: url(../perfil.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: right bottom;
    width: 80%;
    height: 600px;
    border-radius: 30px;
    margin-left: 10px;
}

.about-info {
  margin: 0 50px;
  position: absolute;
  bottom: 33px;
  left: 300px;
}
.about-subtitle {
  margin-bottom: 20px;
  text-align: center;
}
</style>