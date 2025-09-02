<template>
    <div class="container">
    <form @submit.prevent="submitForm">
        <div>
        <label for="firstName">FirstName :</label>
        <input type="text" id="firstName" v-model="firstName" required   />
      </div>
      <div>
        <label for="secondName">secondName :</label>
        <input type="text" id="secondName" v-model="secondName" required   />
      </div>
      <div>
        <label for="phoneNumber">PhoneNumber :</label>
        <input type="number" id="phonenumber" v-model.number="phoneNumber" required   />
      </div>
      <div>
        <label for="email">Email :</label>
        <input type="text" id="email" v-model="email" required   />
      </div>
  
      <div>
        <label for="password">password :</label>
        <input type="password" id="password" v-model="password" required />
      </div>
  
      <button type="submit">LOGIN</button>
    </form>
</div>
  </template>
  <script>
  export default {
    name: 'Formcomponent',
    data() {
      return {
        firstName:'',
        secondName:'',
        phoneNumber:'',
        email: '',
        password: ''

      };
    },
    methods: {
      submitForm() {
        console.log('FirstName', this.firstName)
        console.log('SecondName:', this.secondName)
        console.log('PhoneNumber:', this.phoneNumber)
        console.log('Email:', this.email);
        console.log('Password:', this.password);
      }
    }
  };
  </script>
  
  <style scoped>
  .container{
    background-color: #000;
    width: 600px;
    height: 600px;
    border-radius: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin :30px auto;
  }
  form {
    width: 400px;
    height: 390px;
    margin: auto;
    padding: 20px;
    border: 1px solid #aaa;
    font-family: sans-serif;
    color:#aaa;  
    background-color:#fff;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input {
    width: 100%;
    padding: 8px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
  }
  
  button {
    padding: 10px 15px;
    border: 1px solid #000;
    background: none;
    cursor: pointer;
    background-color: #000;
    color:#aaa;
  }
  </style>