<template>
    <form @submit.prevent="submitForm">
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="name">
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="email">
      <label for="message">Message:</label>
      <textarea id="message" v-model="message"></textarea>
      <button type="submit">Send</button>
    </form>
</template>
  
<script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: ''
      };
    },
    methods: {
      submitForm() {
        // Handle form submission
        alert('Form submitted!');
      }
    }
  };
  </script>
  
  <style scoped>
  form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  
  input, textarea {
    padding: 0.5rem;
    border: none;
    border-radius: 5px;
  }
  
  button {
    padding: 0.5rem;
    border: none;
    border-radius: 5px;
    background-color: #ff5722;
    color: #ffffff;
    cursor: pointer;
  }
</style>
  