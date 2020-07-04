<template>
    <div class="form card-grid">
        <h1 class="form-title" v-if="title">{{ title }}</h1>
        <hr v-if="title">

        <input-group label='Name'>
            <input type="text" name="name" id="name">
        </input-group>

        <input-group label='Email'>
            <input type="email" name="email" id="email">
        </input-group>

        <input-group label='Password'>
            <input type="password" name="password" id="password">
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
        }
    }
}
</script>

<style>
.form .title {
    text-align: center;
}
</style>
