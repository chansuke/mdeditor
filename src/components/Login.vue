<template>
  <div id='login'>
    <h1>{{ msg }}</h1>
    <button>ログイン</button>
  </div>
</template>

<script>
export default {
  name: 'login',
  data() {
    return {
      msg: 'This is a markdown editor'
    };
  }
};
</script>
