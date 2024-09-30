<script setup>
import FirstPage from './components/FirstPage.vue'
import HelloWorld from './components/HelloWorld.vue'
import Task from './components/TaskComponent.vue';
// import TheWelcome from './components/TheWelcome.vue'
</script>
<template>
  <div class="centered">
    <header>
      <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

      <div class="wrapper">
        <HelloWorld msg="I did it!" />
      </div>
    </header>
    
    <main>
      <FirstPage />
      <Task />
    </main>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
.centered {
  display: flex;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  
  .logo {
    margin: 0 2rem 0 0;
  }
  
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>


<!------------------------------ Default Template --------------------------->

<!-- <template>
  <div class="app-wrapper">
    <div>App in Vue.js 3</div>
    <div class="title">{{ firstAppTitle }}</div>
    <div class="cli">{{ cli }}</div>
  </div>
</template>
<script>
export default {
  data(){
   
  components: { FirstPage }, return{
      firstAppTitle: 'My First line in Vue.js 3 - "Hello World"',
      cli: 'Developed using cli instead of cdn link'
    }
  }
}
</script>
<style>
  .title {
    font-weight: bold;
    font-size: x-large;
  }
</style> -->

