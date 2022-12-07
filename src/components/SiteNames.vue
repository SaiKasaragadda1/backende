<template>
   <div class="SiteNames">
        <div v-for="site in sites" :key="site.name">
            <SiteItems :site="site"/>
        </div>
   </div>
</template>

<script>
import SiteItems from './SiteItems.vue'
    export default{
        name:'SiteNames',
        components:{
            SiteItems
        },
        props:{
            sites:Array
        }
    }
</script>


<style scoped>
    .SiteNames{
        background-color: rgb(93, 53, 214);
        padding: 1em;
       max-width: 100%;
       height: auto;
    }
    
    
</style>
