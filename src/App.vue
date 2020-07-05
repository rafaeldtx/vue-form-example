<template>
  <div id="app">
    <Form title='Form Example' />
  </div>
</template>

<script>
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: { Form }
}
</script>

<style>
body {
	background: #0F2027;
    background: -webkit-linear-gradient(to right,
                                       #2C5364, #203A43, #0F2027);
    background: linear-gradient(to right, #2C5364, #203A43, #0F2027);

}

</style>
