<template>
    <div class="game">
        <Display value="1000"/>
        <Button label="Iniciar" @onInitClick="insertPlayer"/>
        <Table />
    </div>
</template>

<script>
import Display from '../components/Display.vue'
import Button from '../components/Button.vue'
import Table from '../components/Table.vue'

export default {
    components: { Button, Display, Table},
    methods: {
        insertPlayer() {
            
        }
    }
}
</script>

<style>

</style>