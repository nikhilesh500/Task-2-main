<template>
  <div class="app-wrapper">
    <div>The below lines are added by me into App in Vue.js 3 using <b>FirstPage Component</b> </div>
    <div class="title">{{ firstAppTitle }}</div>
    <div class="cli">{{ cli }}</div>
  </div>
</template>
<script>
  export default {
    data(){
      return{
        firstAppTitle: 'My First line in Vue.js 3 - "Hello World"',
        cli: 'Developed using cli instead of cdn link'
      }
    }
  }
</script>
<style>
  .app-wrapper {
    margin: 5rem auto;
    text-align: center;
  }
  b {
    font-weight: bold;
  }
  .title {
    font-weight: bold;
    font-size: x-large;
  }
</style>