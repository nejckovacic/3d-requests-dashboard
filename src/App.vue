<script setup>
import Header from './components/Header.vue';
import RequestItem from './components/RequestItem.vue';
import RequestList from './components/RequestList.vue';
</script>

<template>
  <div id="app">
    <Header />
    <RequestList />
  </div>
</template>

<style>
#app {
  max-width: 600px;
  margin: auto;
  padding: 20px;
}
</style>
