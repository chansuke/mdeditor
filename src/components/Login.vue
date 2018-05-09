<template>
  <div id='login'>
    <h1>{{ msg }}</h1>
    <button @click="googleLogin">ログイン</button>
  </div>
</template>

<script>
export default {
  name: 'login',
  data() {
    return {
      msg: 'Welcome to mdeditor'
    };
  },
  methods: {
    googleLogin: function() {
      firebase
        .auth()
        .signInWithRedirect(new firebase.auth.GoogleAuthProvider());
    }
  }
};
</script>
