<template>
    <div class="form card-grid">
        <h1 class="form-title" v-if="title">{{ title }}</h1>
        <hr v-if="title">

        <input-group
            v-for="attribute in attributes"
            :label="attribute.name"
            :key="attribute.name"
        >
            <input type="text" :name="attribute.name" :id="attribute.name">
        </input-group>
    </div>
</template>

<script>
import InputGroup from './InputGroup'

export default {
    components: { InputGroup },
    props: {
        title: {
            type: String,
            default: null
        },
        attributes: {
            type: Array,
            required: true
        }
    }
}
</script>

<style>
.form .title {
    text-align: center;
}
</style>
