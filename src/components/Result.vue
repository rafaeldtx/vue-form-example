<template>
  <div class="result">
      <h1 class="title">Result</h1>
      <hr>
      <div class="group" v-for="(field, index) in attributes" :key="index">
          <span class="title">{{ index }}:</span>
          {{ field || "? ? ?" }}
      </div>
  </div>
</template>

<script>
export default {
    props: {
        attributes: {
            type: Object,
            required: true
        }
    }
}
</script>

<style>
    .result .group {
        font-size: 1.4rem;
        margin: 1.2rem;
    }

    .result-group .title {
        text-transform: capitalize;
    }
</style>
