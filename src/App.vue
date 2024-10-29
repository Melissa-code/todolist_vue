<template>
  <div id="app">
    <componentIndex></componentIndex>
  </div>
</template>

<script>

import ComponentIndex from './components/ComponentIndex/ComponentIndex.vue';

export default {
  name: 'App',
  components: {
    'componentIndex' : ComponentIndex
  }
}
</script>

<style></style>
