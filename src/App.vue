<template>
  <div id="app">
     <MyComponent/>
     <FindName/>
  </div>
</template>

<script>

import MyComponent from './components/MyComponents.vue';
import FindName from './components/FindName.vue';

export default {
  name: 'App',
  components: {
    MyComponent,
    FindName,
}
}
</script>


