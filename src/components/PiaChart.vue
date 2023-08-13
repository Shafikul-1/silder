
<script setup>
import {  onMounted } from 'vue'

let cart = null
const dataSet =  [300, 50, 100]

const data = {
  labels: [
    'Red',
    'Blue',
    'Yellow'
  ],
  datasets: [{
    label: 'My First Dataset',
    data: dataSet,
    backgroundColor: [
      'rgb(255, 99, 132)',
      'rgb(54, 162, 235)',
      'rgb(255, 205, 86)'
    ],
    hoverOffset: 4
  }]
};
const config = {
  type: 'pie',
  data: data,
};
onMounted(() => {
    const ctx = document.getElementById('myChart');
    cart = new Chart(ctx, config)
})

</script>

<template>
    <div>
        <div class="bg-gray-400">
            <canvas id="myChart"></canvas>
        </div>
    </div>
</template>


<style scoped>

</style>
