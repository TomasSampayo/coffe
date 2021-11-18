<template>
  <!-- COFFEE CARDS -->
  <section class="uk-section">
    <div class="uk-container">
      <h2 class="uk-text-center uk-heading-small">
        {{ msg }}
      </h2>

      <div class="uk-position-relative uk-visible-toggle uk-light" tabindex="-1" uk-slider>

        <ul class="uk-slider-items uk-child-width-1-2@s uk-child-width-1-3@m uk-grid uk-grid-match">
          <li v-for="coffee in coffees" v-bind:key="coffee.id">
            <div class="uk-panel">
              <Card v-if="coffee.process === type"
              :name="coffee.name"
              :image="coffee.image"
              :description="coffee.description"
              />
            </div>
          </li>
        </ul>

        <a class="uk-position-center-left uk-position-small uk-hidden-hover" href="#" uk-slidenav-previous uk-slider-item="previous"></a>
        <a class="uk-position-center-right uk-position-small uk-hidden-hover" href="#" uk-slidenav-next uk-slider-item="next"></a>

      </div>
    </div>
  </section>
</template>

<script>
  import Card from "./Card.vue";

  export default {
    name: "CardCarrousel",
    props: ["coffees", "type", "msg"],
    components: {
      Card,
    },
  };
</script>
