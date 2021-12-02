<template>
  <section id="about" 
    class="
    uk-section
      uk-background-secondary
      uk-text-center
      uk-text-left@l
      uk-text-primary
    "
  >
    <div class="uk-container">
      <div class="uk-grid uk-flex-middle" uk-grid>
        <div class="uk-width-3-5@m">
          <h2 class="uk-text-primary uk-heading-small">Sobre Nosotros</h2>
          <p>
            Tenemos preparado un rincón en el corazón de la ciudad
            para que te sientas siempre como en casa.
          </p>
          <p>
            No solo podemos prepararte un café con los granos que elegiste sinó
            que también ofrecemos degustaciones para animarte a encontrar tu 
            próximo café favorito.
          </p>
          
          <adress uk-grid class="uk-margin-medium-top uk-grid uk-child-width-1-2@m">
            
            <div>
              <h3 class="uk-text-primary uk-margin-remove-bottom">Visitá Nuestro Local</h3>
              <ul class="uk-list uk-margin-small-top">
                <li><strong>Dirección</strong> Av. de la Rosa 42026 horario</li>
                <li><strong>Teléfono</strong> <a href="tel:+54123456789">123456789</a></li>
                <li><strong>Horario</strong> 9 a 22 hs</li>
              </ul>
            </div>

            <div>
              <h3 class="uk-text-primary uk-margin-remove-bottom">Contactos</h3>
              <p class=" uk-margin-small-top"><strong>Correo Electrónico</strong> <a href="mailto:somoscafe@gmail.com">somoscafe@gmail.com</a></p>
            </div>

          </adress>
        </div>
        <div class="uk-width-2-5@m">
          <img uk-img src="../assets/images/about-us.png" alt="Somos cafe bar" class="uk-width-1-1" />
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
