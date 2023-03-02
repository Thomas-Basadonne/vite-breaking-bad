<script>
import CardList from "./CardList.vue";
import selectType from "./selectType.vue";
import axios from "axios";

export default {
  components: { CardList, selectType },
  methods: {
    fetchFilteredPage(selectedType) {
      console.log(selectedType);
      axios
        .get(
          "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0&type=${selectedType}"
        )
        .then((response) => {
          console.log(response);
        });
    },
  },
};
</script>
<template>
  <div class="container">
    <selectType @on-select="fetchFilteredPage" />
    <CardList />
  </div>
</template>
<style></style>
