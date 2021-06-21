<template>
    <button class="button"
    @click="$emit('insertPlayer', label)"
        :class="{operation}">
        {{label}}
    </button>
</template>

<script>
export default {
    props: {
        label: {},
        operation: {type: Boolean},
    }
}
</script>

<style>
.button {
    width: 15%;
    height: 50px;
    margin: 5%;
    display: flex;
    justify-content: center;
    align-items: center;
    
}
</style>