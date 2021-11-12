<template>
  <div class="uk-height-viewport uk-background-primary">
    <Navbar />
    <NewCoffeeCardCarrousel />
    <!-- EXPRESSOS -->
    <h2 class="uk-text-center">Expressos</h2>
        <CardCarrousel :coffees="oldCoffees" type="Expresso"/>
    <h2 class="uk-text-center">Lavados</h2>
        <CardCarrousel :coffees="oldCoffees" type="Lavado"/>
    <AboutUs />
  </div>
</template>

<script>
import UIkit from "uikit";
import Icons from "uikit/dist/js/uikit-icons";
import NewCoffeeCardCarrousel from "./components/NewCoffeeCardCarrousel.vue"
import AboutUs from "./components/AboutUs.vue"
import Navbar from "./components/Navbar.vue"
import CardCarrousel from "./components/CardCarrousel.vue"
import axios from "axios";

UIkit.use(Icons);
export default {
  name: "App",
  data() {
    return {
      oldCoffees: null,
    };
  },
  components: {
    NewCoffeeCardCarrousel,
    AboutUs,
    Navbar,
    CardCarrousel
  },
  mounted() {
    axios
      .get("./database.json")
      .then((res) => (this.oldCoffees = res.data.oldCoffees))
      .then((res) => console.log(res));
  },
};
</script>

<style lang="scss">
.badge-radious{
  border-radius: 15px;
}
.badge-size{
  width: 109px;
  height: 31px;
}
.badge-position{
  position: relative;
  top: -60px;
}
.red-background{
  background-color: #FF4848;
}
.text-white{
  color: white; 
}
.title{
  font-family: 'Lato', sans-serif;
  font-size: 36px !important;
  font-weight: 700;
}
.lead{
  font-family: 'Lato', sans-serif;
  font-size: 16px !important;
  font-weight: 400;
  font-style: italic;
}
.img-size{
  width: 250px;
  height: 250px;
}
</style>
