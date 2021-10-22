<template>
  <div>
    <div v-if="results.length === size">
      <p v-for="(result, index) in results" :key="index">
        {{ result }}
      </p>
      <p>Ellapsed Time: {{ ellapsedTime }} ms</p>
    </div>
    <p v-else>loading…</p>
  </div>
</template>

<script>
async function longTask(time) {
  return new Promise((resolve) => {
    setTimeout(() => resolve("long time ended"), time);
  });
}
export default {
  props: {
    size: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      results: [],
      ellapsedTime: 0,
    };
  },
  fetchOnServer: false,
  async fetch() {
    const start = performance.now();
    for (let i = 0; i < this.size; i++) {
      this.results.push(await longTask(3000));
    }
    this.ellapsedTime = performance.now() - start;
  },
};
</script>

<style>
</style>