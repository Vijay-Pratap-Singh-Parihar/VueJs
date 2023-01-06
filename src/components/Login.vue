<script setup>

export default{
    name: "About",
    data() {
        return{
            LoginForm:{
            loginFirstName:"",
                loginLastName:"",
                loginPin:"",
            }
        }
    },
    methods: {
        about:(e){
            console.log(this.LoginForm.loginFirstName, this.LoginForm.loginLastName, this.LoginForm.loginPin)
        }
    }
}
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
      Code:
      <input type="text" v-model="LoginForm.loginPin" name="pinCode" /><br />
      <button v-on:click="about">Submit</button>
    </form>
  </div>
</template>
