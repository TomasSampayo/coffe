<template>
    <div class="uk-card uk-background-secondary">
    <div class="uk-card-media-top">
      <img
        class="uk-align-center uk-margin-xlarge-top img-size"
        v-bind:src="image"
        alt="imagen de la bolsa que contiene {{name}}"
      />
    </div>
    <div class="uk-text-center card-body-position">
      <h3 class="uk-card-title uk-text-primary title">{{ name }}</h3>
      <p class="uk-text-primary lead">"{{ description }}"</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoffeCardsWithType",
  props: ['name', 'description', 'image']
};
</script>
