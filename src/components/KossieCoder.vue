<template>
    <div>
        <p>header</p>
        <slot name="header" :kossie="kossie"></slot> <!-- slot에 name을 지정하면 그 자리에 template로 대체된다. -->
        <!-- kossie라는 이름으로 KossieCoder의 data kossie를 올려보내면 
            AboutView에서 kossie라는 이름으로 사용할 수 있다. -->
        <p>body</p>
        <slot></slot> <!-- slot에 name을 지정하지 않으면 default -->
        <p>footer</p>
        <!-- Slot: 코드 밑에 원하는 html 코드를 따로 넣고 싶을 때 사용-->
    </div>
</template>

<script>
export default ({
    // props: ['title'],
    props: {
        title: {
            type: String,
            default: 'default title',
        },
        name: {
            type: String,
            default: 'default name',
        },
    },

    data() {
        return {
            kossie: 'coder',
        //     //name: 'Kossie Coder',
        }
    },

    methods: {
        // updateName() {
        //     this.name = 'Kossie Coder Updated';
        // }
    }
})
</script>

<style scoped>

</style>
