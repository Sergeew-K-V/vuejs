<template>
  <div class="alco">
    <div class="input__block">
      <label for="ml-input">Milliliters</label>
      <input
        id="ml-input"
        type="text"
        v-model="milliliters"
        placeholder="Insert total milliliters"
      />
    </div>
    <div class="input__block">
      <label for="alco__type-select">Type of alcohol</label>
      <select
        id="alco__type-select"
        v-model="alcoType"
        placeholder="Type of alcohol"
      >
        <option value="Vodka">Vodka</option>
        <option value="Gin">Gin</option>
        <option value="Tequila">Tequila</option>
      </select>
    </div>
    <div class="input__block">
      <label for="volume-input">Volume</label>
      <input
        id="volume-input"
        type="text"
        v-model="volume"
        placeholder="Insert total volume"
      />
    </div>
    <div class="input__block">
      <label for="drinkType-input">Drink Type</label>
      <select
        id="drinkType-input"
        v-model="drinkType"
        placeholder="Type of drink"
      >
        <option value="Standard">Standard</option>
        <option value="Rocks">Rocks</option>
        <option value="Long">Long</option>
      </select>
    </div>
    <div class="btn__block">
      <button @click="this.showRecipe">Check recipe</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlcoCalculatorView",
  data: function () {
    return {
      milliliters: "",
      alcoType: "Gin",
      volume: "",
      drinkType: "Standard",
    };
  },
  methods: {
    showRecipe: function () {
      console.log(this.$data.milliliters);
    },
  },
};
</script>

<style scoped lang="scss">
.alco {
  width: 100%;
  height: 100%;
  padding: 2rem 20rem;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: auto;
  gap: 2rem;
  .input__block {
    max-width: 180px;
    display: flex;
    flex-direction: column;
    align-items: start;
    label {
      padding: 0 0 0.25rem;
    }
    input {
      width: 100%;
      border: 0.25rem solid rgb(73, 73, 214);
      border-radius: 0.5rem;
      padding: 0.2rem;
      &:hover {
        border: 0.25rem solid rgb(32, 32, 180);
      }
    }
    select {
      width: 100%;
      border: 0.25rem solid rgb(73, 73, 214);
      border-radius: 0.5rem;
      padding: 0.2rem;
      &:hover {
        border: 0.25rem solid rgb(32, 32, 180);
      }
    }
  }
  .btn__block {
    display: flex;
    max-width: 100%;
    grid-column-start: 4;
    button {
      margin: 0.25rem 0 0;
      padding: 0.2rem 0.5rem;
      border-radius: 0.5rem;
      background-color: rgb(73, 73, 214);
      border: 0.25rem solid rgb(73, 73, 214);
      text-align: center;
      color: #ffffff;
      transition: all 0.2s ease-in-out;
      cursor: pointer;
      &:hover {
        color: rgb(32, 32, 180);
        background-color: #ffffff;
        border: 0.25rem solid rgb(32, 32, 180);
      }
    }
  }
}
</style>
