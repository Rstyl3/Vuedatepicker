<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
      <button v-on:click="show = !show">
        Show Table
      </button>
      <transition name="fade">
        <Grid v-if="show"/>
      </transition>
  </div>
</template>

<script>
import Grid from './Grid'

export default {
  name: 'HelloWorld',
  components: {
    Grid
  },
  data () {
    return {
      msg: 'Testing Vue!',
      show: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
