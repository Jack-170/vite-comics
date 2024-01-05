<script>
export default {
    name:"cards", 
    props:{
        Comics:Array,
    },
    mounted() {
        console.log('Comics:', this.Comics);
    },
    methods:{
        GetImagePath: function(imgPath){
            return new URL(imgPath, import.meta.url ).href;
        }
    }
    
}

</script>

<template>


    <div class="container">

        <div class="card-box">
            <div class="card" v-for="(comic, index) in Comics" :key="index">
                <div class="box-img">

                    <img :src="GetImagePath(comic.thumb)" alt="Comic Thumbnail">

                   

                </div>

                <p>{{comic.series}}</p>
               
               
            </div>    
        </div>


        
            <h3>LOAD MORE</h3>
        

    </div>
    
    
  
</template>

<style lang="scss" scoped>

@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.container{
    font-size: 16px;
    text-align: center;
    padding: 20px 0;

    h3{
        
        padding: 1rem;
        background-color: #0282f9;
        width: 25%;
        margin: 0 auto;
        
    }

    .card-box{
        margin: 1.5rem 0;
        width: 100%;
        @include wrap;
       
        .card{
            
            width: calc(100% * 1/6 - 15px);
            height: 250px;
            margin-right: 15px;
            margin-top: 10px;
            

            p{
                margin-top: 15px;
            }

            .box-img{
                height: 190px;
                width: 100%;
            }

            
            
        }
    }

   
}



</style>
