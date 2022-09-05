<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-if="goal.show">{{ goal.text }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoals">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script setup>
import {
  // ref,
  reactive,
} from 'vue';

// const goal = 'Complete the course and master Vue.';

// const goal = ref('Complete the course and master Vue.');
// const showGoals = ref(true);

const goal = reactive({
  show: true,
  text: 'Complete the course and master Vue.',
});

function toggleGoals() {
  // showGoals.value = !showGoals.value;
  goal.show = !goal.show;
}
// export default {
//   data() {
//     return {
//       showGoals: true,
//       goal: 'Complete the course and master Vue.',
//     };
//   },
//   methods: {
//     toggleGoals() {
//       this.showGoals = !this.showGoals;
//     },
//   },
// };
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
