<template>
    <!-- NEW COFFEE CARDS -->
    <div v-if="coffees">
      <div class="uk-slider-container-offset uk-background-secondary" uk-slider>
        <div
          class="uk-position-relative uk-visible-toggle uk-light"
          tabindex="-1"
        >
          <ul class="uk-slider-items uk-child-width-1-2@s uk-grid">
            <li v-for="coffee in coffees.newCoffees" v-bind:key="coffee.id">
              <NewCoffeeCard :title="coffee.name" :img="coffee.image" :lead="coffee.description"/>
            </li>
          </ul>

          <a
            class="uk-position-center-left uk-position-small uk-hidden-hover"
            href="#"
            uk-slidenav-previous
            uk-slider-item="previous"
          ></a>
          <a
            class="uk-position-center-right uk-position-small uk-hidden-hover"
            href="#"
            uk-slidenav-next
            uk-slider-item="next"
          ></a>
        </div>
        <ul class="uk-slider-nav uk-dotnav uk-flex-center uk-margin"></ul>
      </div>
    </div>
    <div v-else>
      <p>Loading...</p>
    </div>
</template>

<script>
import axios from "axios";
import NewCoffeeCard from "./NewCoffeeCard.vue"
export default {
  name: "NewCoffeeCardCarrousel",
  data() {
    return {
      coffees: null,
    };
  },
  components: {
    NewCoffeeCard
  },
  mounted() {
    axios
      .get("./database.json")
      .then((res) => (this.coffees = res.data))
      .then((res) => console.log(res));
  },
};
</script>