<template>
    <div class="container">
        <h2>Counter component</h2>
        <div class="card-panel teal lighten-2 " id="counter">
            <h4>Counter: {{ counter }}</h4>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Counter', 
        data: function() {
             return {
                counter: 0
            }
        },
        mounted() {
            setInterval(() => {
                this.counter++
            }, 1000)
        }
    }
</script>

<style scoped>

</style>

