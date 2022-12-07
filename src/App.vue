<template>
  <div class="container">
    <!-- Step 3 you must use the imported component-->
    <HeaderTop TopicName= " TOP SOCIAL MEDIA NETWORKS"/>
    <SiteNames :sites="sites"/>
  </div>
</template>

<script>
// Step 1: import HeaderTop.vue
import HeaderTop from './components/HeaderTop.vue'
import SiteNames from './components/SiteNames.vue'
export default{

  name: 'App',
  components: {
    HeaderTop,
    SiteNames
  },
  data(){
    return {
      sites:[]
    }
  },
  methods:{
    async fetchBooks(){
      const res=await fetch("https://nodeserver.herokuapp.com/api")
      const data=await res.json()
      console.log(data)

      return data.sites
    }
   
  },
  async created(){
      this.sites=await this.fetchBooks()
    }

    // Step 2: Register the imported component 

}
  
</script>


<style >
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  

  body{
    font-family: "Montserrat", sans-serif;
  }
  .container{
    max-width: 700px;
    max-height: 1000px;
    margin:  30px auto;
    overflow: auto;
    min-height: 300px;
    border: 0.4em solid black;
    padding: 30px;
    border-radius: 5px;
    color:red;
    background-color: rgb(147, 233, 110);
    font-size: 15px;
  }

</style>