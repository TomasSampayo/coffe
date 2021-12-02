<template>
  <div id="NewCoffeeCard" class="uk-card uk-card-body uk-card-secondary uk-text-center y">
    
      <img
    class="uk-align-center uk-border-circle"
    v-bind:src="img"
    alt="imagen de la bolsa que contiene {{title}}"
    />
      
      <!--NEW COFFEE BADGE -->
    <span class="uk-label uk-label-danger uk-text-large uk-label-new">
      Nuevo
    </span>

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

    <button
      class="uk-button uk-button-default uk-button-primary"
      :uk-toggle="`target: #NewCoffeModal`"
      type="button"
    >
      Ver Más
    </button>

    <!-- MODAL -->

    <div id="NewCoffeModal" uk-modal>
      <div
        class="
          uk-modal-dialog uk-background-secondary uk-text-primary uk-text-center uk-text-left@s
        "
      >
        <!-- HEADER -->
        <div class="uk-modal-header uk-background-secondary ">
           <button class="uk-modal-close-default" type="button" uk-close></button>
          <h2
            class="uk-modal-title uk-text-primary"
          >
            {{ title }}
            <span class="uk-label uk-label-danger uk-margin-left">Nuevo</span>
          </h2>
        </div>
        <!-- BODY -->
        <div class="uk-modal-body">
          <img
            class="uk-align-center img-size"
            v-bind:src="img"
            alt="imagen de la bolsa que contiene {{title}}"
          />
          <p class="uk-text-italic">{{ lead }}</p>

          <ul class="uk-list uk-list-disc">
            <li><strong>Origen</strong> {{ origin }}</li>
            <li><strong>Process</strong> {{ process }}</li>
            <li><strong>Weight</strong> {{ weight }}</li>
          </ul>
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
