<template>
    <div>
       <p>Header</p>
        <slot name="header" :kossie="kossie"></slot>
        <!--slot 선언해주고 
            views 파일에서 <Hyeon>사이에 아무말이나 써준다</Hyeon> 
        -->
        <p>Body</p>
        <slot></slot>
        <p>footer</p>
        <!-- <button @click="updateName"> change name</button> -->
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
                kossie: "coder"
            // name : "HYEON's PAGE",
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