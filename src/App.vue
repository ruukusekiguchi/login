<template>
  <div id="app">
    <div id="new">
      <p>ユーザ名</p>
      <input type="text" v-model="item" v-on:keydown.enter="onKeyDown">
      <p>パスワード</p>
      <input type="text" v-model="pass" v-on:keydown.enter="onKeyDown">
      <button @click="newSend">登録</button>
    </div>

    <div id="login">
      <p>ユーザ名</p>
      <input type="text" v-on:keydown.enter="onKeyDown">
      <p>パスワード</p>
      <input type="text" v-on:keydown.enter="onKeyDown">
      <button @click="loginSend">ログイン</button>
    </div>
    <p>{{ user.newitem }}</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      item: "",
      pass: "",
      users: [],
    };
  },
  methods: {
    onKeyDown() {
      this.newSend();
    },
    newSend(){
      if(this.item == "" || this.pass == ""){
        alert("未入力はやめてくださいよ");
        return;
      }
      for(i = 0; i < this.newid;i++){
        count++;
      }
      var user = {
        newid: this.count + 1,
        newitem: this.item,
        newpass: this.pass,
      };
      this.users.push(user);
      // this.item = "";
    }
  }
}
</script>

<style>
#app {

}
</style>
