<template>
  <div class="container">
    <h1>Learning Accessibility</h1>
    <form autocomplete="on">
      <div class="input-wrapper">
        <input
            type="text"
            placeholder="Username"
            id="user"
            class="form-input">
        <label
            for="user"
            class="form-label">
          Username</label>
      </div>
      <div class="input-wrapper">
        <input type="text" placeholder="Password" id="pass" class="form-input">
        <label for="pass" class="form-label">Password</label>
      </div>
      <div class="input-wrapper md:span-2">
        <input type="email" placeholder="Email" id="email" class="form-input">
        <label for="email" class="form-label">Email</label>
      </div>
      <button type="submit" class="btn md:span-2">Sign Up</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,

  },
  data() {
    return {
      clicked: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



</style>
