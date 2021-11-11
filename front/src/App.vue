<template>
  <div class="uk-height-viewport uk-background-primary">
    <Navbar />
    <NewCoffeeCardCarrousel />
    <!-- EXPRESSOS -->
    <h2 class="uk-text-center">Expressos</h2>
    <div v-for="coffee in oldCoffees" :key="coffee.name">
      <div>
        <Card v-if="coffee.process == 'Expresso'" name="coffee.name" description="coffee.description" image="coffee.image"/>
      </div>
    </div>
    <!-- NATURALES -->
    <h2 class="uk-text-center">Naturales</h2>
    <div v-for="coffee in oldCoffees" :key="coffee.name">
      <div v-if="coffee.process == 'Natural'">
        <Card :name="coffee.name" description="coffee.description" image="coffee.image"/>
      </div>
    </div>
    <!-- LAVADOS -->
    <h2 class="uk-text-center">Lavados</h2>
    <div v-for="coffee in oldCoffees" :key="coffee.name">
      <div v-if="coffee.process == 'Lavado'">
        <Card :name="coffee.name" description="coffee.description" image="coffee.image"/>
      </div>
    </div>
    <AboutUs />
  </div>
  
</template>

<script>
import UIkit from "uikit";
import Icons from "uikit/dist/js/uikit-icons";
import NewCoffeeCardCarrousel from "./components/NewCoffeeCardCarrousel.vue"
import Card from "./components/Card.vue"
import AboutUs from "./components/AboutUs.vue"
import Navbar from "./components/Navbar.vue"
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
    Card,
    AboutUs,
    Navbar
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
