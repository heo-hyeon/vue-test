<template>
    <div>
        <h1> {{ title }}</h1>
        <p> {{ name }}</p>
        <button @click="updateName"> change name</button>
    </div>
</template>

<script>
    export default {
        props : {
            title: {
                type: String,
                // required: true
                default : 'default title'
            },
            test : {
                type: String,
                default: 'default test'
            },
        },

        data () {
            return {
        name : "HYEON's PAGE",
            }
        },

        methods : {
            updateName () {
                this.name = "HYEON updated";
            }
        }
    }
</script>

<style>
</style>