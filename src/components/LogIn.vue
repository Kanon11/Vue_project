<template>
  <div>
    <h1>Login</h1>
    <p v-bind:class="{ paragraph: isActive == 1 }">{{ message }}</p>
    <br />

    <input type="text" v-model="message" /><br /><br />
    <p v-bind:class="{ paragraph: isActive == 1 }">{{ count }}</p>
    <br />
    <button v-on:click="count++">+</button><br />
    <button @click="count--">-</button>
  </div>
</template>

<script>
export default {
  name: "LogIn",
  watch:{
    count(){
        alert("value changed")
    }
  },
  data:()=> {
    return {
      name: "kanon",
      message: "hi",
      isActive: true,
      count: 0,
    };
  },
  beforeCreate() {
    console.log("bofore|Created", this.name);
  },
  created() {
    console.log("created", this.name);
  },
  methods: {
    kk: function() {
      alert("click");
    },
  },
};
</script>

<style>
.paragraph {
  color: red;
  background-color: aliceblue;
}
</style>