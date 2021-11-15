<template>
  <div class="uk-height-viewport uk-background-primary">
    <div class="uk-container uk-container-small">
      <Navbar />
      <NewCoffeeCardCarrousel />
      <!-- EXPRESSOS -->
      <h2 class="uk-text-center uk-margin-xlarge-top uk-heading-small header">
        Expressos
      </h2>
      <CardCarrousel :coffees="oldCoffees" type="Expresso" />
      <div :v-if="oldCoffees">
        <!-- <div v-for="cafe in lavados(oldCoffees)" :key="cafe.name">dagggllgcffs</div> -->
      </div>
      <h2 class="uk-text-center uk-margin-xlarge-top uk-heading-small header">
        Lavados
      </h2>
      <CardCarrousel :coffees="oldCoffees" type="Lavado" />
    </div>
    <AboutUs />
  </div>
</template>

<script>
import UIkit from "uikit";
import Icons from "uikit/dist/js/uikit-icons";
import NewCoffeeCardCarrousel from "./components/NewCoffeeCardCarrousel.vue";
import AboutUs from "./components/AboutUs.vue";
import Navbar from "./components/Navbar.vue";
import CardCarrousel from "./components/CardCarrousel.vue";
import axios from "axios";

UIkit.use(Icons);
export default {
  name: "App",
  data() {
    return {
      oldCoffees: null,
      expressos: null,
    };
  },
  components: {
    NewCoffeeCardCarrousel,
    AboutUs,
    Navbar,
    CardCarrousel,
  },
  mounted() {
    axios
      .get("./database.json")
      .then((res) => (this.oldCoffees = res.data.oldCoffees))
  },
  methods: {
    lavados(coffeeList) {
      return coffeeList.filter((coffee) => coffee.process === "Lavado");
    },
  },
};
</script>

<style lang="scss" scope>
.badge-radious {
  border-radius: 15px;
}
.badge-size {
  width: 109px;
  height: 31px;
}
.badge-position {
  position: relative;
  top: -60px;
}
.red-background {
  background-color: #ff4848;
}
.text-white {
  color: white;
}
.header {
  font-family: "Lato", sans-serif;
}
.title {
  font-family: "Lato", sans-serif;
  font-size: 36px !important;
  font-weight: 700;
}
.lead {
  font-family: "Lato", sans-serif;
  font-size: 16px !important;
  font-weight: 400;
  font-style: italic;
}
.img-size {
  width: 250px;
  height: 250px;
}
</style>
