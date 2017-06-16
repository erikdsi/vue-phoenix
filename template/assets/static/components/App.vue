<template lang="pug">
  #main
    h1 Here's your app
    #main-content
      router-view

</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
@import '../css/app.scss';

#main {
  width: 80%;
  margin: 0 auto;
}
</style>
