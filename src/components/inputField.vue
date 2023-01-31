<template>
    <div>
        <label for="">Name</label>
        <input 
        type="text" 
        :value="name"
        style="padding:30px; border:2px solid green"
        @input="updateName"    
        >
    </div>  
</template>
<script>
    export default {
        props : {
            name : {
                type:String,
                required: true
            }
        },
        methods : {
            updateName (e) {
                console.log(e.target.value);
                this.$emit('update-name',e.target.value);
                // emit을 쓰면 부모 컨포넌트로 값을 보내준다.
                // 1. 부모 컨포넌트는 HomeView.vue파일에서 
                // 2. vue rounter 마지막 코드막을때 @update-name="updateName"를 써주고
                // 3. updateName 함수를 만들어준다.
            }
        }
    }
</script>