<template>
  <div class="about">
    <h1>This is an about page</h1>
    <pre @click="forOh">{{oh}}</pre>
  </div>
</template>

<script>
// @ is an alias to /src
// import {get} from 'axios'

export default {
  data() {
    return {
      oh: 'no oh'
    }
  },
  name: 'About',
  mounted() {
    this.forOh()
  },
  methods: {
    forOh() {
      this.oh = 'oh loading...'
      // get(`/oh?r=${Date.now()}`).then(res => {
      //   this.oh = res.data.oh + Date.now()
      // }).catch(err => console.log('oh Err', err.message, err.name))
    }
  }
}
</script>
