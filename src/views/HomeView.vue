<template>
  <div>
    <h1>This is Home page</h1>
    <form action="">
      <InputField :name="name" @update-name="updateName" />
      <br><button>Submit</button>
    </form>
    {{ name }}
  </div>
  <!-- 자식 컴포넌트에서 이벤트로 받아온 @update-name 값을 받아와서 업데이트 한다.  -->
</template>

<script>
import InputField from '@/components/InputField.vue';
export default {
  components: {
    InputField
  },
  data() {
    return {
        name: ''
    }
  },
  methods: {
    updateName(name) {
      this.name = name;
    }
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>



