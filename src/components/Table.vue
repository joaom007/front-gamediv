<template>
    <table class="table">
        <thead>
            <tr>
                <th>Nome</th>
                <th>Chutes</th>
                <th>Tempo</th>
            </tr>
        </thead>
        <tbody>
            <!-- <tr v-for="game in games">
                <td>{{game.player.name}}</td>
                <td>{{game.gameSeconds}}</td>
                <td>{{game.plays.name}}</td>

            </tr> -->
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
.table {
   
}
</style>