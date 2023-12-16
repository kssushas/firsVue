<template>
  <div class="find">
   <p>I will find u!</p>
   <input type="text" v-model="search" placeholder="enter names">
   <p>{{ information }}</p>
   <ul>
    <li v-for="name in filteredNames" :key="name">{{ name }}</li>
   </ul>

  </div>
</template>

<script>
 export default{
    name: 'FindName',
    data(){
        return {
            search : '',
            coincidence: 0,
            names : ['Vanya', 'Ks', 'Ira', 'Dima', 'Valeriy'],
        }
    },
    computed: {
        information(){
            return `Amount of names: ${this.names.length} Coincidence: ${this.filteredNames.length}`;
        },
        filteredNames(){
            return this.names.filter(name => name.toLowerCase().startsWith(this.search.toLowerCase()));
        },
    }
 }
</script>