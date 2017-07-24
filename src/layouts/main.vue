<template>
  <div class="container">
    <div class="nav" id="myNav">
      <ul>
        <li v-for="link in links">
          <v-link :href="link.href">{{link.name}}</v-link>
        </li>
      </ul>
    </div>

    <div class="main-content">
      <div class="header">
        <slot name="header"></slot>
      </div>
      
      <div>
        <slot name="content"></slot>
      </div>
    </div>

  </div>

</template>


<script>
  import VLink from '../components/VLink.vue'

  export default {
    components: {
      VLink
    },
    data () {
      return {
        links: [
          {href:'/', name: 'Home'},
          {href:'/blog', name: 'Blog'},
          {href:'/newBlog', name: 'New-blog'}
        ]
      }
    }
  }


</script>


<style scoped>
  .container {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
  }

  .nav {
    position: fixed;
    float: left;
    width: 20%;
    height: 100%;
    box-shadow: 1px 1.5px 1px 1.5px #DDDDDD;
    padding: 10px;
    overflow-y: scroll;
    overflow-x: hidden;
  }

  .nav ul {
    list-style: none;
  }

  .nav li {

  }

  p {
    margin: 0;
  }

  .main-content {
    width: 80%;
    height: 100%;
    float: right;
  }

  .header {
    width: 100%;
    height: 2.5em;
    background-color: #4A8CF6;
    padding: 0.5em;
    color: white;
  }

  .content {
    overflow-y: scroll;
    overflow-x: hidden;
  }



</style>
