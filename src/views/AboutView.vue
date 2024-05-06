<template>
  <div class="about">
    <h1>This is an about page</h1>
    <KossieCoder>
        <!-- <template v-slot:header> --> <!-- KossieCoder의 header라는 이름은 가진 slot으로 대체된다. -->
        <!-- # 으로 대체 가능하다. -->
          <template #header="{ kossie }"> 
          <p>header11 {{ kossie }}</p>
          <!-- KossieCoder.vue에서 보낸 kossie라는 속성을 받아서 사용할 수 있다. -->
        </template>

        <template v-slot:default>
          hello11
        </template>
    </KossieCoder>
  </div>
</template>

<script> 
import KossieCoder from '@/components/KossieCoder.vue';

export default {
  components: {
    KossieCoder
  },
  
}
</script>