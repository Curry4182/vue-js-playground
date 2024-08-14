<template>
  <div>
    <form @submit.prevent="submitLogin">
      <div>
        <label for="userId">ID:</label>
        <input id="userId" type="text" v-model="userId">
      </div>
      <div>
        <label for="password">PW:</label>
        <input id="password" type="text" v-model="password">
      </div>
      <button type="submit">로그인</button>
    </form>
  </div>
</template>

<script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        userId: '',
        password: '',
      }
    },
    methods: {
      submitLogin() {
        const data = {
          'userId': this.userId,
          'password': this.password
        };

        axios.post('https://jsonplaceholder.typicode.com/users', data)
          .then(res => {
            console.log(res)
          });
      }
    }
  }
</script>

<style scoped>

</style>