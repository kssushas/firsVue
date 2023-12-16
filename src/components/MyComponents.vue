<template>
  <div>
    <p>Enter the value</p>
    <button @click="clickOnMin">-</button>
    <select v-model="selectedValue">
      <option v-for="val in data" :key="val" :value="val">{{ val }}</option>
    </select>
    <button @click="clickOnMax">+</button>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  data() {
    return {
      data: [0, 1, 2, 3],
      selectedValue: 0,
    };
  },
  methods: {
    clickOnMin() {
      if (this.selectedValue > 0){
         this.selectedValue = this.selectedValue - 1;
      }
    },
    clickOnMax() {
      if (this.selectedValue < this.data[this.data.length-1]){

      this.selectedValue = this.selectedValue + 1;
      }
    },
  },
};
</script>
