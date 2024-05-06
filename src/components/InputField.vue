<template>
    <div>
        <label for="">Name</label>
        <input 
            type="text" 
            :value="name"
            style="padding: 30px; border: 2px solid green;"
            @input="updateName"
        >
    </div>
    <!-- @input: 유저가 input필더에 값을 삽입해서 변했을 때 발동 -->
    <!-- 값이 변화했을 때 @input의 updateName함수를 실행하면서 
        this.$emit('update-name', e.target.value)에 의해 부모로 value를 보내준다. -->
    <!-- @input="this.$emit('update-name', $event)" 로 바로 보내도 된다.
        부모 컴포넌트인 HomeView.vue에선 <InputField :name="name" @update-name="name = $event.target.value" /> 라고 수정해야함 -->
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true
        }
    },
    methods: {
        updateName(e) {
            console.log(e.target.value);
            this.$emit('update-name', e.target.value);
        }
    }
}
</script>
