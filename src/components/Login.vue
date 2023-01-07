<script>
export default {
  data() {
    return {
      LoginForm: {
        loginFirstName: null,
        loginLastName: null,
        loginPin: null,
      },
    };
  },
  methods: {
    login(e) {
      console.log(
        this.LoginForm.loginFirstName,
        this.LoginForm.loginLastName,
        this.LoginForm.loginPin
      );
    },
  },
};
</script>

<template>
  <div>
    <form @submit.prevent="getFormValue">
      First Name:
      <input type="text" v-model="LoginForm.loginFirstName" name="fname" />
      <br />
      Last Name:
      <input type="text" v-model="LoginForm.loginLastName" name="lname" />
      <br />
      Pin Code:
      <input type="text" v-model="LoginForm.loginPin" name="pinCode" /><br />
      <button v-on:click="login">Submit</button>
    </form>
  </div>
</template>
