<script>
export default {
  data() {
    return {
      loginType: "username" // keep lowercase to match <option value>
    }
  }
}
</script>

<template>
  <h1>Please select your login option</h1>

  <!-- Dropdown bound to loginType -->
  <select v-model="loginType">
    <option value="username">Username login</option>
    <option value="email">Email login</option>
  </select>

  <!-- Conditional rendering -->
  <div v-if="loginType === 'username'">
    <label>Username</label>
    <input placeholder="Enter your username" />
  </div>

  <div v-else-if="loginType === 'email'">
    <label>Email</label>
    <input type="email" placeholder="Enter your email" />
  </div>
</template>
