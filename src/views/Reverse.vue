<template>
  <div class="reverse">
    <h1>This is the Reverse Page</h1>
    <h2>Enter your string to reverse:</h2>
    <label>String:
      <input type="text" id="string" v-model.lazy="message">
    </label>
    <h2>the reversed message is:</h2>
    <p> {{ reversedMessage }} </p>
  </div>
</template>

<script>
  export default {
    name: 'Reverse',
    data (){
      return {
        message: ''
      }
    },
  computed: {
    reversedMessage() {
      return this.message.split('').reverse().join('');

    }
  }

}
</script>
