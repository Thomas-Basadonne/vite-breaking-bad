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
  <div class="card col gx-3">
    <img :src="pic" alt="" class="img-fluid" />
    <h5>{{ name }}</h5>
    <p>{{ type }}</p>
  </div>
</template>
<style></style>
