<template>
    <div class="container">
        <h2>Hover effect component</h2>
        <p>Example of attribute binding. Here, a message appears while hovering the text for a few seconds.</p>
        <div class="row">
            <div class="col s12 m6 offset-m3">
                <div id="bind-attribute" class="card-panel teal">
                    <span v-bind:title="message" class="white-text">
                        Hover your mouse over me for a few seconds to see my dynamically-bound
                        title! 
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HoverMessage',
    data() {
        return {
            message: 'Secret message: You loaded this page on ' + new Date().toLocaleString()
        }
    }
}
</script>

<style scoped>
</style>