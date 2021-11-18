<template>
  <div class="uk-card uk-card-body uk-card-secondary uk-text-center">

    <img
    class="uk-align-center"
    v-bind:src="img"
    alt="imagen de la bolsa que contiene {{title}}"
    />

    <!--NEW COFFEE BADGE -->
    <span class="uk-label uk-label-danger uk-text-large uk-label-new">
      Nuevo
    </span>

    <h3 class="uk-card-title uk-margin-remove-bottom">{{ title }}</h3>
    <p class="uk-text-lead uk-margin-remove-top">"{{ lead }}"</p>
    
  </div>
</template>

<script>
  export default {
    name: "NewCoffeeCard",
    props: ["title", "lead", "img"],
  };
</script>
