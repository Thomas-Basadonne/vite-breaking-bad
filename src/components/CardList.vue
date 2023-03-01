<script>
import card from "./card.vue";
import axios from "axios";

export default {
  data() {
    return {
      characters: [],
    };
  },

  components: {
    card,
  },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0")
      .then((response) => {
        console.log(response);
        this.characters = response.data.data;
        console.log(this.characters);
      });
  },

  components: { card },
};
</script>
<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid bg-dark py-2">
      <select
        class="form-select"
        aria-label="Default select example"
        style="width: 20%"
      >
        <option selected>Seleziona il Type</option>
        <option value="1">One</option>
        <option value="2">Two</option>
        <option value="3">Three</option>
      </select>
    </div>
  </nav>
  <div
    class="row row-cols-5 d-flex justify-content-between container mx-0 gy-4"
  >
    <card
      class="text-center"
      v-for="character in characters"
      :pic="character.card_images[0].image_url"
      :name="character.name"
      :type="character.type"
    />
  </div>
</template>
<style></style>
