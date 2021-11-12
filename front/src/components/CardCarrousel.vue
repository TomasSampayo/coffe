<template>
  <!-- COFFEE CARDS -->
    <div class="uk-slider-container-offset uk-background-secondary" uk-slider>
      <div
        class="uk-position-relative uk-visible-toggle uk-light"
        tabindex="-1"
      >
        <ul class="uk-slider-items uk-child-width-1-2@s uk-grid">
          <li v-for="coffee in coffees" v-bind:key="coffee.id">
            <Card v-if="coffee.process == type"
              :name="coffee.name"
              :image="coffee.image"
              :description="coffee.description"
            />
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
    
  

</template>

<script>
import Card from "./Card.vue";

export default {
  name: "CardCarrousel",
  props: ["coffees", "type"],
  components: {
    Card,
  },
};
</script>
