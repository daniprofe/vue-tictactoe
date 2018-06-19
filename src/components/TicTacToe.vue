<template>

    <div>

        <div id="actual-player-container">
            <span id="actual-player-char">{{turn}}</span>
            <span id="actual-player-name">{{players[turn]}}</span>
        </div>

        <table class="playfield">
            <tr>
                <td>{{status[0][0]}}</td>
                <td>{{status[0][1]}}</td>
                <td>{{status[0][2]}}</td>
            </tr>
            <tr>
                <td>{{status[1][0]}}</td>
                <td>{{status[1][1]}}</td>
                <td>{{status[1][2]}}</td>
            </tr>
            <tr>
                <td>{{status[2][0]}}</td>
                <td>{{status[2][1]}}</td>
                <td>{{status[2][2]}}</td>
            </tr>
        </table>

    </div>

</template>

<script>

export default {
    name: 'TicTacToe',
    data: function () {
        return {
            players: {
                'X': 'player 1',
                'O': 'player 2'
            },
            turn: 'X',
            status: [
                ['', '', ''],
                ['', '', ''],
                ['', '', '']
            ]
        };
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

    .playfield {

        margin: auto;
        border-collapse: separate;
        border-spacing: 10px;
        background-color: aqua;

        td {
            width: 100px;
            height: 100px;
            background-color: white;
        }

    }

</style>
