<template>
  <div class="reverse">
    <h1>This is a reverse page</h1>
    <h2>Please enter a string to reverse!</h2>
    <label for="input-string"></label> 
      <input type="text" id="input-string" v-model.lazy="message">

  <p>{{reveredMessage}}</p>
  </div>
</template>
<script>
export default {
  name:"Reverse",
  data(){
    return {
      message:''
    }
  },
  computed: {
    reveredMessage() {
      return this.message.split('').reverse().join('');
    }
  }
}
</script>
