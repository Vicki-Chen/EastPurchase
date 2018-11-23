<template>
  <div class="home">
    {{msg}}
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Home'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('../../../styles/main.less');
.home{
  color:red;
}
</style>
