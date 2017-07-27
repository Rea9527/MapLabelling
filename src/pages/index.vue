<template>
  <main-layout>
  	<div slot="header">
  		<p>Welcome home</p>
  	</div>

  	<div slot="content">
  		
  	</div>
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/main.vue'
  // import Caman from 'caman'
  Caman= require('caman')

  export default {
    components: {
      MainLayout
    },

    methods: {
      loadImg: function() {
        Caman();
      }
    }
  }
</script>

<style scoped>

</style>