<template>
  <div>
    <h1>Sequential Promises</h1>
    <SequentialPromises :size="10" />
    <h1>Parallel Promises</h1>
    <ParallelPromises :size="10" />
  </div>
</template>

<script>
import SequentialPromises from "../components/sequentialpromises";
import ParallelPromises from "../components/parallelpromises";

export default {
  components: {
    SequentialPromises,
    ParallelPromises,
  },
};
</script>

<style>
</style>