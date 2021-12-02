<template>
  <div class="uk-card uk-card-small uk-background-secondary">
    <div class="uk-card-media-top">
      <img
        width="180"
        height="180"
        class="uk-align-center uk-margin-medium-top image-radious-circle"
        v-bind:src="img"
        alt="imagen de la bolsa que contiene {{title}}"
      />
      <!--HEADER -->
      <div
        class="
          badge-radious badge-size
          red-background
          uk-align-center
          badge-position
          uk-margin-remove-bottom
        "
      >
        <p class="uk-text-center text-white">NUEVO</p>
      </div>
    </div>
    <div class="uk-text-center card-body-position">
      <h3 class="uk-card-title">{{ title }}</h3>
      <p
        class="
          uk-text-primary
          lead
          uk-margin-medium-left uk-margin-medium-right
        "
      >
        "{{ lead }}"
      </p>
    </div>
    <button
      class="uk-align-center uk-button uk-button-default uk-button-primary"
      :uk-toggle="`target: #ID`"
      type="button"
    >
      Ver Más
    </button>

    <!-- MODAL -->

    <div id="ID" uk-modal>
      <div
        class="
          uk-modal-dialog uk-modal-body uk-background-secondary uk-text-primary
        "
      >
        <!-- HEADER -->
        <div class="uk-modal-header uk-background-secondary">
          <h2
            class="uk-modal-title uk-text-primary uk-text-center uk-text-left@s"
          >
            {{ title }}
          </h2>
        </div>
        <!-- BODY -->
        <div class="uk-modal-body">
          <img
            class="uk-align-center img-size"
            v-bind:src="img"
            alt="imagen de la bolsa que contiene {{title}}"
          />
          <div
            class="
              badge-radious badge-size
              red-background
              uk-align-center
              badge-position
              uk-margin-remove-bottom
            "
          >
            <p class="uk-text-center text-white">NUEVO</p>
          </div>
          <p class="uk-text-italic uk-text-center uk-text-left@s">{{ lead }}</p>
        </div>
        <ul>
          <li><strong>Origen</strong> {{ origin }}</li>
          <li><strong>Process</strong> {{ process }}</li>
          <li><strong>Weight</strong> {{ weight }}</li>
        </ul>
        <!-- FOOTER -->
        <div
          class="
            uk-modal-footer
            uk-background-secondary
            uk-text-center
            uk-text-left@s
          "
        >
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
  name: "NewCoffeeCard",
  props: ["title", "lead", "img", "process", "origin", "weight", "coffeeId"],

  data() {
    return {
      coffee: null,
    };
  },
  // methods: {
  //   getCoffee() {
  //     let allCoffees;
  //     let coffee;
  //     fetch("./database.json").then((res) => (allCoffees = res.data)).then(res => console.log(res))
  //     //coffee = allCoffees.filter((coffee) => coffee.id === id)
  //     console.log(allCoffees)
  //     return coffee;
  //   }
  // },
};
</script>
