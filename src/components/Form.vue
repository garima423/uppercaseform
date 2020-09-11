<template>
  <h2>Converts your input into UpperCase</h2>
  <input type="text" class="input" v-model="lowerInput" @keyup="myFunction()" />
  <div class="teal">
    <br />
    <div class="center ">
      {{ upperInput }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      lowerInput: "",
      upperInput: "",
    };
  },
  methods: {
    myFunction() {
      console.log(this.lowerInput);
      this.upperInput = this.lowerInput.toUpperCase();
    },
  },
};
</script>

<style scoped>
.input {
  height: 30px;
  width: 250px;
  border: 2px solid teal;
  border-radius: 5px;
  box-shadow: 5px 10px teal;
  margin-top: 150px;
}
.teal {
  color: teal;
  font-weight: bold;
}
</style>
