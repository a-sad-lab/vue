<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <pre @click="forHi">{{hi}}</pre>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import {get} from 'axios'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data() {
    return {
      hi: 'no hi'
    }
  },
  name: 'Home',
  methods: {
    forHi() {
      this.hi = 'hi loading...'
      // get(`/hi?r=${Date.now()}`).then(res => {
      //   this.hi = res.data.hi + Date.now()
      // }).catch(err => console.log('hi Err', err.message, err.name))
    }
  },
  components: {
    HelloWorld
  }
}
</script>
