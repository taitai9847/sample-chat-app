<template>
  <div class="chat">
    <h1>This is an chat page</h1>
    <h2>Message is</h2>
    <div class="chatField">
      <div v-for="(text, index) in chat" :key="text+index">
          <p>{{ text }}</p>
      </div>
    </div>
    <footer>
        <div class="inputTextFIeld">
            <input v-model="text" placeholder="Message">
            <button @click="click(text)">send</button>
        </div>
    </footer>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  data: function() {
      return {
          text: '',
          chat: [] as string[]
      }
  },
  methods: {
      click(inputText: string) {
          if (this.text !== '') {
              console.log(inputText)
              this.chat.push(inputText)
              this.text = ''   
          } else {
              alert('文字を入力してください！')
              console.error('input error')
          }
      }
  }
});
</script>

<style>
input {
    -webkit-appearance: none;
    border-radius: 0;
    width: 56%;
    height: 50px;
}
button {
    height: 55px;
    width: 8%;
}
.chatField {
    background-color:whitesmoke;
    height: 500px;
    margin-right: 250px;
    margin-left: 250px;
    overflow: scroll;
}
</style>