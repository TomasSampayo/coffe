<template>
  <nav class="uk-navbar-container uk-navbar-transparent" uk-navbar>
    <div class="uk-navbar-left">
      <ul class="uk-navbar-nav">
        <a class="uk-navbar-item uk-logo" href="#">
          <img src="../assets/logo.png" alt="" />
        </a>
      </ul>
    </div>
    <div class="uk-navbar-right">
      <ul class="uk-navbar-nav">
        <li>
          <a href="">
            <p>About Us</p>
          </a>
        </li>
        <li>
          <a class="uk-navbar-item uk-logo" href="#">
            <img src="../assets/search.png" alt="" />
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped></style>
