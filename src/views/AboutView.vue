<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Hyeon>
      <template #header="props">
        <!-- v-slot:header를 줄여서 #header로 쓴다 -->
        <p>header 슬롯 {{ props.kossie }}</p>
        <!-- props.kossie는 Hyeon.vue에서 올려준 date:kossie 값 -->
      </template>
     
      <template #default>
        hello
      </template>
    </Hyeon>
  </div>
</template>

<script>
import Hyeon from '@/components/Hyeon.vue';

export default {
  components : {
    Hyeon
  }

}
</script>
