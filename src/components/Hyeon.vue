<template>
    <div>
        <p> {{ name }}</p>
        <button @click="updateName"> change name</button>
    </div>
</template>

<script>
    export default {
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