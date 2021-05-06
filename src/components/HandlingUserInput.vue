<template>
    <div class="container">
        <h2>Handling user input</h2>
        <p>This example shows how datas can be transformed with the <b>v-on</b> directive by invoking methods on our instances.</p>
        <div class="row">
            <div class="col s12 m6 offset-m3">
                <div class="card blue-grey darken-1">
                    <div class="card-content white-text">
                        <span class="card-title">{{ message }}</span>
                    </div>
                </div>
                <div class="card-action">
                   <a v-on:click="reverseMessage" class="waves-effect waves-light btn">reverse</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HandlingUserInput',
    data() {
        return {
            message: 'This text can be reversed!'
        }
    },
    methods: {
        reverseMessage() {
            this.message = this.message
                .split('')
                .reverse()
                .join('')
        }
    }
}
</script>
