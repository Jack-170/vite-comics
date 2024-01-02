<script>
export default{
    name:"IconsSection",

    props:{
        Icons:Array,
    },

    
    methods:{
        GetImagePath: function(imgPath){
            return new URL(imgPath, import.meta.url ).href;
        }
    }
    
 }

</script>

<template>


    <div class="icons-section">
        <div class="container">
            <ul>
                <li v-for="(icon, index) in Icons" :key="index">
                    <div class="box-icon">
                        <img :src="GetImagePath(icon.src)" :alt="icon.text">
                    </div>

                    
                        <p>{{icon.text}}</p>
                  
                </li>
                
            </ul>
        </div>

    </div>
    
    
    
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.icons-section{
    height: 130px;
    width: 100%;
    background-color: #0282f9;
    font-size: 15px;

    .container{
        @include align-center;


        ul{
            width: 100%;
            @include space-between;
            list-style-type:none;

            li{
                display: flex;
            }

        }
    }
}




.box-icon{
    width: 35px;
    height: 45px;
}



p{
    color: white;
    @include align-center;
    margin-left:12px;
}




</style>
