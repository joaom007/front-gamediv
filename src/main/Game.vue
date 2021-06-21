<template>
    <div class="game">
        <Input />
        <Display value="1000"/>
        <Button label="Iniciar" @onInitClick="insertPlayer"/>
        <h1>Ranking</h1> 
        <Table />
        
    </div>
</template>

<script>
import Display from '../components/Display.vue'
import Button from '../components/Button.vue'
import Table from '../components/Table.vue'
import Input from '../components/Input.vue'

export default {
    components: {Button, Display, Table, Input},
    methods: {
        insertPlayer() {
            
        }
    }
}

</script>

<style>

</style>