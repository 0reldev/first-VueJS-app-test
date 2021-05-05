<template>
    <div class="container">
        <h2>Simple attribute binding</h2>
        <p>Example of attribute binding. Here, the text title (appearing while hovering the text for a few seconds) is defined with the "message" property as a reactive behvior to the rendered DOM.</p>
        <div class="row">
            <div class="col s12 m6 offset-m3">
                <div id="bind-attribute" class="card-panel teal">
                    <span v-bind:title="message" class="white-text text-to-hover">
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
    .text-to-hover:hover {
        color: palegoldenrod !important;
    }
</style>