<script>
export default {
  data() {
    return {
      id: "demo1",
      blueBox: true   // start as blue
    }
  },
  methods: {
    changeColor() {
      this.blueBox = !this.blueBox; // toggle on click
    }
  }
}
</script>

<template>
  <div class="container">
    <div
      :id="id"
      class="m-2"
      :class="blueBox ? 'blueBox' : 'redBox'"
    >
      div ID : {{ id }}
    </div>

    <button
      type="button"
      :class="blueBox ? 'btn btn-primary' : 'btn btn-danger'"
      @click="changeColor"
    >
      Change Color
    </button>
  </div>
</template>

<style scoped>
.redBox {
  background-color: red;
}
.blueBox {
  background-color: blue;
}
#demo1 {
  color: white;
}
</style>
