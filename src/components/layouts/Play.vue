<template>
    <div>
       <!-- <div class="scoreBoard">
            <span>O has {{ wins.O }} wins</span>
            <h2>Score Board</h2>
            <span>X has {{ wins.X }} wins</span>
        </div>-->
        <div class="app">
            <!--<div id="details">
                <h1>Tic Tac Toe</h1>
                <h2>Match #{{ matches + 1 }}</h2>
            </div>-->
            <grid></grid>
            <button class="restart" @click="restart">Restart</button>
        </div>
    </div>
</template>

<script>
    import Grid from '@/components/layouts/Grid.vue'

    export default {
        components: { Grid },
        name: 'app',
        data () {
            return {
                matches: 0,
                wins: {
                    O: 0,
                    X: 0
                }
            }
        },

        methods: {
            restart () {
                Event.$emit('clearCell')

                Event.$emit('gridReset')

                this.matches++
            }

        },

        created () {
            Event.$on('win', winner => this.wins[winner]++)
            Event.$emit('clickWin', this.wins);
            Event.$emit('win', this.activePlayer)
        }
    }
</script>

<style>
    .app {
        margin: 0 auto;
        width: 500px;
        color: #34495e;
    }

    .restart {
        background-color: #e74c3c;
        color: #fff;
        border: 0px;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        font-family: 'Dosis', Helvetica, sans-serif;
        font-size: 1.4em;
        font-weight: bold;
        margin: 0px;
        padding: 15px;
        width: 100%;
    }
    .restart:hover {
        background-color: #c0392b;
        cursor: pointer;
    }



</style>
