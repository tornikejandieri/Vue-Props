<template>
  <user-data @set-data="addUser"></user-data>
  <active-user
    v-for="user in users"
    :key="user.id"
    :name="user.name"
    :age="user.age"
  ></active-user>
</template>

<script>
export default {
  data() {
    return {
      users: [{ id: "", name: "", age: "" }],
    };
  },
  methods: {
    addUser(user) {
      this.users.push(user);
    },
  },
};
</script>

<style>
/* here would go styles if I weren't lazy :D */
</style>
