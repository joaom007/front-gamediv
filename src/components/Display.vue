<template>
    <div class="display">
        {{name}}
    </div>
</template>

<script>
export default {
    props: ['name']
}
</script>

<style>
    .display {
        width: 15%;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #0004;
        margin: 5%;
    }
</style>