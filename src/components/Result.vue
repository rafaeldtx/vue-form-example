<template>
  <div class="card-grid">
      <div class="result-group" v-for="field in result" :key="field.name">
          <span class="title">{{ field.name }}:</span>
          {{ field.value || "? ? ?" }}
      </div>
  </div>
</template>

<script>
export default {
    props: {
        result: {
            type: Array,
            required: true
        }
    }
}
</script>

<style>
    .result-group {
        font-size: 1.4rem;
        margin: 1.2rem;
    }

    .result-group .title {
        text-transform: capitalize;
    }
</style>
