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

<!-- components 파일
필요한 태그 : <template>, <script>, <style> -->

<!-- div 아이디에 app으로 선언했으면 위치를 나타내는 el에서 "#app"으로 연결시켜준다. -->

<!-- v-for : 반복문 (data에 들어간 items가 있으면 item in items)
     v-on : 이벤트핸들링 (methods) @로만 쓰일수도 있다. 
     v-model : 데이터바인딩 (data)  -->