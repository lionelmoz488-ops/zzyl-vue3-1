<template>
  <div>
    <h1>这是父组件内容：</h1>
    <h1>以下是子组件：</h1>
    <child :message="parentMessage" @message-sent="handleMessage"></child>
  </div>
</template>

<script setup>
import child from './child.vue';

const parentMessage = '来自父组件的消息';

function handleMessage(message){
  console.log('接收到了子组件的消息:', message);
}
</script>