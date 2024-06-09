<template>
  <body>
    <form action="">
      <input type="text" v-model="userName" placeholder="name">
      <input type="password" v-model="userPassword" placeholder="password">
      <input type="email" v-model="userEmail" placeholder="email">
      <p className="error">{{ error }}</p>
      <button @click="sendData()">Send</button>
    </form>

    <User v-for="(el, i) in users" :key="i" :user="el" :deleteUser="deleteUSer"/>

  </body>
</template>

<script>
  import User from './components/User.vue'
  export default {
    components: { User },
    data() {
      return {
        users: [],
        error: '',
        userName: '',
        userPassword: '',
        userEmail: ''
      }
    },
      methods: {
        sendData() {
          if(this.userName == '') {
            this.error = 'Name not submited';
            return
          } else if(this.userPassword == '') {
            this.error = 'Password not submited';
            return
          } else if(this.userEmail == '') {
            this.error = 'Email not submited';
            return
          }
          this.error = ''
          this.users.push({
            name: this.userName,
            password: this.userPassword,
            email: this.userEmail
          })
      },
      deleteUser(index) {
        this.user.splice(index, 1)
      }
    }
  }
</script>

<style scoped>
</style>
