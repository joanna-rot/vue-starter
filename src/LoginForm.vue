<template>
  <div>
    <label>Zaloguj się e-mailem</label>
    <input type="email" v-model="email">
    <button @click="enter()">{{buttonLabel}}</button>
  </div>
</template>

<script>

export default {

  data() {
    return {
      email: ''
    }
  },
  methods: {
    enter() {
      this.$emit('login', this.email);
    }
  },
  props: {buttonLabel: String}
}

</script>

<style scoped>

</style>