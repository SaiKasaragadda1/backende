<template>
    <div>
        
        <h1>{{site.Name}}</h1><br>
        <h3><u>Founders:</u>  {{site.Founders}}</h3>
        <h3><u>Launched Year:</u>  {{site.LaunchedYear}}</h3>
        <h3><u>Users:</u>  {{site.NoofUsers}} Billions</h3>
        <h3><u>Revenue:</u>  {{site.Revenue}} Billions</h3>
        <h3><u>HeadQuarters:</u>  {{site.HeadQuarters}}</h3>
        <h3><u>URL:</u>  <a href="site.url">{{site.url}}</a></h3>
         <h3><u>Rank:</u>  {{site.Rank}}</h3>
        
    </div>
    

</template>

<script>
    export default{
        name:'SiteItems',
        props:{
            site: Array
        }
    }
</script>

<style scoped>
    h3{
        margin: 7px;
        
    }
    h1{
        border: 3px solid black;
        background-color: rgb(221, 242, 242);
    }

   
    div{
        background-color:white;
        color: black;
        padding: 1em;
        margin: 5px;
        font-weight: bold;
        font-size: 15px;
    
    }
    
</style>
