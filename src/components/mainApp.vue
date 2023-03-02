<script>
import CardList from "./CardList.vue";
import selectType from "./selectType.vue";
export default {
  components: { CardList, selectType },
};
</script>
<template>
  <div class="container">
    <selectType />
    <CardList />
  </div>
</template>
<style></style>
