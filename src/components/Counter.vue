<template>
  <div>
    <p>{{ currentValue }}</p>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  //   data() {
  //     return {
  //       currentValue: 0,
  //     };
  //   },
  methods: {
    increment() {
      //   this.currentValue = this.currentValue + 1;
      this.$store.commit("INCREMENT_COUNTER");
    },
    decrement() {
      //   this.currentValue = this.currentValue - 1;
      this.$store.commit("DECREMENT_COUNTER");
    },
  },
  computed: {
    currentValue() {
      return this.$store.state.currentValue;
    },
  },
};
</script>

<style scoped></style>
