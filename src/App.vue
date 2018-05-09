<template>
  <div id='app'>
    <Login v-if='!isLogin'></Login>
    <Editor v-if='isLogin' :user="userData"></Editor>
  </div>
</template>

<script>
import Login from './components/Login.vue';
import Editor from './components/Editor.vue';

export default {
  name: 'app',
  data() {
    return {
      isLogin: false,
      userData: null
    };
  },
  created: function() {
    firebase.auth().onAuthStateChanged(user => {
      if (user) {
        this.isLogin = true;
        this.userData = user;
      } else {
        this.isLogin = false;
        this.userData = null;
      }
    });
  },
  components: {
    Login: Login,
    Editor: Editor
  }
};
</script>
