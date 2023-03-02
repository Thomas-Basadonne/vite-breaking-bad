<script>
export default {
  data() {
    return {
      cardsStyle: [
        "Effect Monster",
        "Flip Effect Monster",
        "Flip Tuner Effect Monster",
        "Gemini Monster",
        "Normal Monster",
        "Normal Tuner Monster",
        "Pendulum Effect Monster",
        "Pendulum Effect Ritual Monster",
        "Pendulum Flip Effect Monster",
        "Pendulum Normal Monster",
        "Pendulum Tuner Effect Monster",
        "Ritual Effect Monster",
        "Ritual Monster",
        "Spell Card",
        "Spirit Monster",
        "Toon Monster",
        "Trap Card",
        "Tuner Monster",
        "Union Effect Monster",
        "Fusion Monster",
        "Link Monster",
        "Pendulum Effect Fusion Monster",
        "Synchro Monster",
        "Synchro Pendulum Effect Monster",
        "Synchro Tuner Monster",
        "XYZ Monster",
        "XYZ Pendulum Effect Monster",
        "Skill Card",
        "Token",
      ],

      selectedType: "",
    };
  },

  emits: ["on-select"],

  methods: {
    selectType() {
      this.$emit("on-select", this.selectedType);
    },
  },
};
</script>
<template>
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid bg-dark py-2">
      <select
        class="form-select"
        aria-label="Default select example"
        style="width: 20%"
        v-model="selectedType"
        @change="selectType"
      >
        <option v-for="style in cardsStyle">{{ style }}</option>
      </select>
    </div>
  </nav>
</template>

<style></style>
