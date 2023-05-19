<script setup>
import LineChartExample from "../components/LineChartExample.vue";
import MultiLineChartExample from "../components/MultiLineChartExample.vue";
import BarsChartExample from "../components/BarsChartExample.vue";
import { markRaw, reactive, ref } from "vue";

const LineChartExampleS = markRaw(LineChartExample)
const MultiLineChartExampleS = markRaw(MultiLineChartExample)
const BarsChartExampleS = markRaw(BarsChartExample)

const component = ref(LineChartExampleS)

</script>
<template>
  <div class="flex">
    <div class="grid h-20">
      <div class="text-left p-4">
        <h1 class="text-xl font-semibold">Examples</h1>
      </div>
      <button @click="component = LineChartExampleS" class="text-left ml-4 p-2 border rounded-md mb-2">
        LineChart
      </button>
      <button @click="component = MultiLineChartExampleS" class="text-left ml-4 p-2 border rounded-md mb-2">
        MultiLineChart
      </button>
      <button @click="component = BarsChartExampleS" class="text-left ml-4 p-2 border rounded-md mb-2">
        BarChart
      </button>
    </div>
    <div class="w-full m-5">
      <component :is="component" />
    </div>
  </div>
  <div></div>
</template>
