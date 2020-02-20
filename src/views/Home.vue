<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <customTextarea id="test" row="4" column="10" name="form" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';
import customTextarea from '@/components/textarea.vue';

export default {
  name: 'Home',
  components: {
    HelloWorld,
    customTextarea
  }
}
</script>
