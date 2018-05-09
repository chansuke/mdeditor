<template>
  <div id='add'>
    <Login v-if='!isLogin'></Login>
    <Editor v-if='isLogin'></Editor>
  </div>
</template>

<script>
import Login from './components/Login.vue';
import Editor from './components/Editor.vue';

export default {
  name: 'app',
  data() {
    return {
      isLogin: false
    };
  },
  components: {
    Login: Login,
    Editor: Editor
  }
};
</script>
