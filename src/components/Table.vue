<template>
    <table class="table">
        <thead>   
            <tr>
                <th>Nome</th>
                <th>Tempo (s)</th>
                <th>Chutes</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(game, i) in games" :key="i">
                <td>{{game.player.name}}</td> 
                <!-- <td>{{game.plays}}</td>  -->
                <td>{{game.gameSeconds}}</td>
            </tr>
        </tbody>
    </table>
</template>

<script>
export default {
    props: {
        label: {},
        operation: {type: Boolean},
        games: null
    },
    methods: {
        getgames() {
            fetch('http://localhost:8081/games')
                .then(resp => resp.json())
                .then(data => this.games = data)
        }
    },
    mounted() {
        this.getgames()
    }
}
</script>

<style>

</style>