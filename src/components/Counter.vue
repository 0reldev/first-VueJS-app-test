<template>
    <div class="container">
        <h2>Counter component</h2>
        <div class="card-panel teal lighten-2 " id="counter">
            <h4>Counter: {{ counter }}</h4>
            <div class="row">
                <div class="col s6">
                    <a @click="restart" class="waves-effect waves-light btn"><i class="material-icons left">replay</i>Restart</a>
                </div>
                <!-- <div class="col s6">
                    <a @click="stop" class="waves-effect waves-light btn"><i class="material-icons left">pause</i>Stop</a>
                </div> -->
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Counter', 
        data() {
        //data: function() {   //  Cette ligne équivaut celle du dessus.
            return {
                counter: 0,
            }
        },
        mounted() {
            setInterval(() => {
                this.counter++            
            }, 1000)
        },
        methods: {
            restart() {
                this.counter = 0;
            },
        }
    }
</script>

<style scoped>

</style>

