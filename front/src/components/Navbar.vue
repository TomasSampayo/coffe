<template>
  <div class="uk-container">
    <nav class="uk-navbar-container uk-navbar-transparent" uk-navbar>
      <div class="uk-navbar-left">
        <a class="uk-navbar-item uk-logo" href="#">
          <img src="../assets/images/logo.png" alt="Logo" />
        </a>
      </div>

      <div class="nav-overlay uk-navbar-right">
        <ul class="uk-navbar-nav uk-visible@s">
          <li><a href="#about" uk-scroll>Sobre nosotros</a></li>
        </ul>

        <a
        class="uk-navbar-toggle"
        uk-search-icon
        uk-toggle="target: .nav-overlay; animation: uk-animation-fade"
        href="#"
        ></a>
      </div>

      <div class="nav-overlay uk-navbar-left uk-flex-1" hidden>

        <div class="uk-navbar-item uk-width-expand">
          <form class="uk-search uk-search-navbar uk-width-1-1">
            <input
            class="uk-search-input"
            type="search"
            placeholder="Buscar café..."
            autofocus
            />
          </form>
        </div>

        <a
        class="uk-navbar-toggle"
        uk-close
        uk-toggle="target: .nav-overlay; animation: uk-animation-fade"
        href="#"
        ></a>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: "Navbar",
  };
</script>

<style scoped></style>
