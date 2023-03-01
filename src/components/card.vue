<script>
export default {
  props: {
    pic: String,
    name: String,
    type: String,
  },
};
</script>
<template>
  <div class="card col text-bg-warning" style="width: 15rem">
    <img :src="pic" alt="" class="img-fluid" />
    <h5 class="text-light">{{ name }}</h5>
    <p>{{ type }}</p>
  </div>
</template>
<style></style>
