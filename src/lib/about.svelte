
<script>
export let mail = '';
export let phone = '';
export let adress = '';
</script>

<div class="about-container">
  <ul>
    <li>
      <span>Nombre</span>
      <p>Gabriel Pérez</p>
    </li>
    <li>
      <span>Cumpleaños</span>
      <p>26 de Mayo, 1987</p>
    </li>
    <li>
      <span>Mail</span>
      <p>{mail}</p>
    </li>
    <li>
      <span>Teléfono</span>
      <p>{phone}</p>
    </li>
    <li>
      <span>Dirección</span>
      <p>{adress}</p>
    </li>
    <li>
      <span>Nacionalidad</span>
      <p>Española</p>
    </li>
  </ul>
</div>

<style>
.about-container {
  background-color: var(--color-main);
  border-radius: 20px;
  padding: 20px;
  width: max-content;
}

.about-container ul li {
  list-style: none;
  color: #ffff;
  margin: 15px 0px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.about-container p {
  font-size: 1.3rem;
  font-weight: bold;
  padding-top: 5px;
}
.about-container span {
  font-size: 1rem;
  margin-bottom: 10px;
}
</style>