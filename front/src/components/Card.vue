<template>
  <div>
    <div class="uk-card uk-card-body uk-card-secondary uk-card-hover">
      <div class="uk-card-media-top">
        <img
          width="180"
          height="180"
          class="uk-align-center image-radious-circle"
          v-bind:src="img"
          alt="imagen de la bolsa que contiene {{title}}"
        />
      </div>
      <div class="uk-text-center card-body-position">
        <h4 class="uk-card-title">{{ title }}</h4>
        <p class="uk-text-primary lead">"{{ lead }}"</p>
        <button
          class="uk-align-center uk-button uk-button-default uk-button-primary"
          uk-toggle="target: #my-id"
          type="button"
        >
          Ver Más
        </button>
      </div>
      <!-- MODAL -->
    </div>
    <div id="my-id" uk-modal>
      <div
        class="
          uk-modal-dialog uk-modal-body uk-background-secondary uk-text-primary
        "
      >
        <div class="uk-modal-header uk-background-secondary">
          <h5 class="uk-modal-title uk-text-primary">{{ title }}</h5>
        </div>
        <div class="uk-modal-body">
          <img
            class="uk-align-center img-size"
            v-bind:src="img"
            alt="imagen de la bolsa que contiene {{title}}"
          />
          <p class="uk-text-italic">{{ lead }}</p>
        </div>
        <ul>
          <li><strong>Origen</strong> {{ origin }}</li>
          <li><strong>Process</strong> {{ process }}</li>
          <li><strong>Weight</strong> {{ weight }}</li>
        </ul>
        <div class="uk-modal-footer uk-background-secondary">
          <button
            class="
              uk-modal-close
              uk-button
              uk-button-default
              uk-button-primary
              uk-text-secondary
            "
            type="button"
          >
            Cerrar
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoffeCardsWithType",
  props: ["title", "lead", "img", "process", "origin", "weight", "coffeeId"],
};
</script>
