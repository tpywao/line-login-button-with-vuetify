<template lang="pug">
  v-app#app(:dark="dark")
    v-tooltip(top)
      v-btn(icon slot="activator" @click="dark = !dark")
        <v-icon>invert_colors</v-icon>
      <span>invert colors</span>
    v-layout
      v-flex
        div
          v-btn(large)
            | large
        div
          v-btn
            | normal
        div
          v-btn(disabled)
            | disabled
        div
          v-btn(small)
            | small
      v-flex
        div
          line-login-button(large)
        div
          line-login-button
        div
          line-login-button(disabled)
        div
          line-login-button(small)
      v-flex.box
        div
          div
            line-login-button(large)
        div
          div
            line-login-button
        div
          div
            line-login-button(small)
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      dark: false,
    }
  },
}
</script>

<style lang="sass">
#app
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  .box div > div
    background-color: grey
    display: inline-block
    margin: 1px
</style>
