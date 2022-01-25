<template>
  <div class="Hero container">
    <div class="text-container">
      <h3 class="header">Find Your Fire Extinguisher</h3>
      <p class="snippet">
        Fire extinguishers apply an agent that will cool burning heat, smother
        fuel or remove oxygen so the fire cannot continue to burn. A portable
        fire extinguisher can quickly control a small fire if applied by an
        individual properly trained. <span style="color: red">{{ data1 }}</span>
      </p>

      <button  class="button btn">Start Here</button>
    </div>
    <img
      src="~/assets/svg/fire-extinguisher.svg"
      alt="fire-extinguuisher"
      class="image"
    />
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState(["data1", "data3"]),
  },
};
</script>

<style scoped>
.Hero {
  height: 50vh;
  position: relative;
  display: flex;
  padding: 3rem 0;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 13rem;
}
.text-container {
  width: 50%;
  margin-top: 0.4rem;
}
.header {
  font-weight: 900;
  font-size: 3rem;
}
.snippet {
  color: grey;
  font-size: 1.25rem;
}
.image {
  width: 20rem;
  margin-top: 0.4rem;
}
.overlay {
  background: rgba(0, 0, 0, 0);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.button {
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  width: 20rem;
  font-weight: 700;
  transition: 0.5s;
}
.button:hover {
  width: 21.5rem;
}
@media (max-width: 500px) {
  .Hero {
    height: 40vh;
  }
}
</style>