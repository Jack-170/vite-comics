<script>
export default {
    name:"Jumbotron",

    methods:{
        GetImagePath: function(imgPath){
            return new URL(imgPath, import.meta.url ).href;
        }
    }
    
}

</script>

<template>

    <div class="jumbo">

        
       

    </div>
    
    
  
</template>

<style lang="scss" scoped>

@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.jumbo{
    width: 100%;
    height: 250px;
    background-image: url(../assets/images/jumbotron.jpg);
    background-size: cover;
}





</style>
