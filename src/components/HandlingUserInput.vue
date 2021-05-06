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
        <br/><br/>
        <p>Thanks to the <b>v-model</b> directive, a dynamic text can be displayed which can be edited in an text input area. The displayed text is synchronized and updated in real time with the edition.</p>
        <div class="row">
            <div class="col s12 m6 offset-m3">
                <div class="card brown darken-4">
                    <div class="card-content white-text">
                        <span class="card-title">{{ personalMessage }}</span>
                    </div>
                </div>
                <br/>
                <div class="input-field">
                    <input v-model="personalMessage" id="personal_message" type="text" class="validate">
                    <label for="personnal_message">Write your message here:</label>
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
            message: 'This text can be reversed!',
            personalMessage: 'Write your own message.'
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
