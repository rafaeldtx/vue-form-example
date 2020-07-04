<template>
    <div class="input-group">
        <label>{{ label }}:</label>
        <div class="input">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    props: ['label']
}
</script>

<style scoped>
    .input-group {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin: 5px 0px;
        font-size: 1.4rem;
    }

    .input {
        display: flex;
        align-self: stretch;
        margin: 10px 0px;
    }

    input, textarea, select {
        flex: 1;
        font-size: 1.4rem;
        outline: none;
        border: 1px solid #DDD;
        border-radius: 5px;
        padding: 5px 10px;
    }


    input:focus {
        border: 1px solid #BBB;
    }
</style>
