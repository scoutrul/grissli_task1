<template>
  <div class="hello">
    <h2>Объем</h2>
    <div>{{ counted }}</div>
    <button @click="count">рассчитать </button>
  </div>
</template>

<script>
export default {
  name: "Bottle",
  props: {
    fillIn: {
      type: Number,
      require: false,
      default: () => 0
    },
    fillOut: {
      type: Number,
      require: false,
      default: () => 0
    },
    vol: {
      type: Number,
      require: false,
      default: () => 1000
    }
  },
  computed: {
    counted(){
      return +this.fillIn + -this.fillOut
    }
  },
  methods: {
    count(){
      if(this.counted < 0) {
        alert('переслив')
      }
      else if(this.counted > this.vol) {
        alert('перелив')
      }
      else {
        alert(`в бутылке ${this.counted} ml`)
      }
    }   
  }
};
</script>

<style scoped></style>
