<template>
  <div class="uk-card uk-background-secondary">
    <div class="uk-card-media-top">
      <img
        class="uk-align-center uk-margin-xlarge-top img-size"
        v-bind:src="img"
        alt="imagen de la bolsa que contiene {{title}}"
      />
      <!--NEW COFFEE BADGE -->
      <div
        class="
          badge-radious badge-size
          red-background
          uk-align-center
          badge-position
        "
      >
        <p class="uk-text-center text-white">NUEVO</p>
      </div>
    </div>
    <div class="uk-text-center card-body-position">
      <h3 class="uk-card-title uk-text-primary title">{{ title }}</h3>
      <p class="uk-text-primary lead">"{{ lead }}"</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewCoffeeCard",
  props: ["title", "lead", "img"],
};
</script>
