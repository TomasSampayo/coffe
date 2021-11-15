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
        <div class="uk-width-3-5">
          <h2 class="uk-text-primary uk-heading-medium uk-margin-top">Sobre Nosotros</h2>
          <p class="text">
            Tenemos preparado un rincón en el corazón de la ciudad
            para que te sientas siempre como en casa.
          </p>
          <p class="text">
            No solo podemos prepararte un café con los granos que elegiste sinó
            que también ofrecemos degustaciones para animarte a encontrar tu 
            próximo café favorito.
          </p>
          <div uk-grid>
            <div>
              <h2 class="uk-text-primary">Visitá Nuestro Local</h2>
              <p class="text">
                dir Av. de la Rosa 42026 <br />tel 123456789 <br />horario 9 a
                22 hs
              </p>
            </div>
            <div>
              <h2 class="uk-text-primary">Contactos</h2>
              <p><b>Mail:</b>somoscafe@gmail.com</p>
            </div>
          </div>
        </div>
        <div class="uk-width-2-5 uk-flex uk-flex-middle">
          <img uk-img src="../assets/about-us.svg" alt="Somos cafe bar" />
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
