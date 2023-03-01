<script>
import card from "./card.vue";
import axios from "axios";

export default {
  data() {
    return {
      characters: [],
    };
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
  <!-- <card /> -->

  <div class="row row-cols-5">
    <div class="col text-center" v-for="character in characters">
      <img :src="character.card_images[0].image_url" alt="" class="img-fluid" />
      <h5>{{ character.name }}</h5>
      <p>{{ character.type }}</p>
    </div>
  </div>
</template>
<style></style>
