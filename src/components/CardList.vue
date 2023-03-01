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
  <div class="row row-cols-5">
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
