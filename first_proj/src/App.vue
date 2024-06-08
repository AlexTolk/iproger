<script>
  export default {
    data() {
      return {
        info: 'Lorem',
        moreInfo: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sequi natus id reiciendis?'
      }
    },
      methods: {
        userData() {
          this.info = 'Changed the info'
        }
    }
  }

</script>

<template>
  <body>
    <h3>{{ info }}</h3>
    <p>{{ moreInfo }}</p>
    <button type="button" @click="userData()">Change</button>
  </body>
</template>

<style scoped>
  h3 {
    font-weight: lighter;
    color:aliceblue;
  }
  p {
    color:crimson;
  }
</style>
