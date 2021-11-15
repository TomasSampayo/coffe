<template>
  <nav class="uk-navbar-container uk-navbar-transparent" uk-navbar>
    <div class="uk-navbar-left">
      <a class="uk-navbar-item uk-logo" href="#">
        <img src="../assets/logo.png" alt="" />
      </a>
    </div>
    <div class="nav-overlay uk-navbar-right">
      <p>Nuestro Local</p>
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
            placeholder="Search"
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
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped></style>
