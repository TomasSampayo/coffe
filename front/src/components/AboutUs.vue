<template>
  <section
    class="
      uk-background-secondary
      uk-text-left@l
      uk-text-center@s
      uk-text-primary
      uk-margin-xlarge-top
    "
  >
    <div class="uk-container uk-container-small">
      <div class="uk-grid-small" uk-grid>
        <div class="uk-child-width-1-3">
          <h2 class="uk-text-primary">Sobre Nosotros</h2>
          <p class="text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer at
            ultricies urna, quis porttitor ante. Donec tempor justo vel ligula
            accumsan, quis gravida felis congue.
          </p>
          <p class="text">
            Duis fermentum, odio sit amet interdum egestas, tortor odio semper
            purus, dignissim consectetur est nulla a magna. Morbi eget arcu
            enim. Maecenas porta tortor in porta fermentum.
          </p>
          <div uk-grid>
          <h2 class="uk-text-primary">Visitá Nuestro Local</h2>
          <p class="text">
            dir Av. de la Rosa 42026 <br />tel 123456789 <br />horario 9 a 22 hs
          </p>
          <h2 class="uk-text-primary">Contactos</h2>
          <p><b>Mail:</b>somoscafe@gmail.com</p>
          </div>
        </div>
        <div>
          <img uk-img src="../assets/about-us.png" alt="Somos cafe bar" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutUs",
};
</script>

<style scoped>
.text {
  font-family: "Lato", sans-serif;
  font-weight: 300;
  font-size: 16px;
}
</style>
