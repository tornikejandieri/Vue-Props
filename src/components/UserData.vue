<template>
  <form action="" @submit.prevent="outPutData">
    <label for="name">Name</label>
    <input type="text" v-model="enteredName" />
    <label for="age">Age</label>
    <input type="text" v-model="enteredAge" />
    <button>submit</button>
  </form>
</template>

<script>
export default {
  emits: ["set-data"],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    outPutData() {
      const randomId = this.enteredName + Math.floor(Math.random() * 1000) + 1;
      this.$emit("set-data", {
        id: randomId,
        name: this.enteredName,
        age: this.enteredAge,
      });
    },
  },
};
</script>
