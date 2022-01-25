<template>
  <div>
    <b-button id="toggle-btn" @click="toggleModal">Rent</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="d-block text-center">
        <!-- <h3>Hello From My Modal!</h3> -->
        <div class="calendar-container">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Cupiditate, nihil asperiores modi est, exercitationem assumenda id
            quo dolorum aspernatur laboriosam iste quidem sint quos cum
            necessitatibus adipisci temporibus? Hic, vitae.
          </p>
          <vc-date-picker :value="null" color="indigo" is-dark is-range />
        </div>
        <b-button id="show-btn" @click="()=>{
            addItem(product.id)
            hideModal()
          }">Order</b-button>
      </div>
      <!-- <b-button class="mt-3" variant="outline-danger" block @click="hideModal"
        >Close Me</b-button
      > -->
      <!-- <b-button
        class="mt-2"
        variant="outline-warning"
        block
        @click="toggleModal"
        >Toggle Me</b-button
      > -->
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'
export default {
  props:['product'],
  methods: {
    showModal() {
      this.$refs["my-modal"].show();
    },
    hideModal() {
      this.$refs["my-modal"].hide();
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs["my-modal"].toggle("#toggle-btn");
    },
    ...mapMutations(['addItem'])
  },
};
</script>
<style scoped>
button {
  width: 100%;
  border: none;
  padding: 0.5rem;
  color: white;
  font-weight: 700;
  padding: 1rem 4rem;
  border-radius: 100rem;
  background-color: rgb(231, 81, 43);
  color: white;
  font-weight: 700;
  transition: 0.5s;
}
.calendar-container {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
p {
  color: grey;
}
.text-container {
  padding: 0.5rem;
}
</style>