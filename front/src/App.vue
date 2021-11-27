<template>
  <div>
    <Navbar />
      
    <NewCoffeeCardCarrousel />

    <!-- EXPRESSOS -->
    <CardCarrousel :coffees="oldCoffees" type="Expresso" msg="Expresso" />

      <!-- <div :v-if="oldCoffees">
        <div v-for="cafe in lavados(oldCoffees)" :key="cafe.name">dagggllgcffs</div>
      </div> -->
      
      <!-- Lavados -->
      <CardCarrousel :coffees="oldCoffees" type="Lavado" msg="Lavado" />

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
      computed: {
        Expressos() {
          return this.oldCoffees ? this.coffees.filter((coffee) => coffee.process === "Expresso") : "Loading..."
        }
      }
    };
  </script>

  <style lang="scss" scope>
  </style>
