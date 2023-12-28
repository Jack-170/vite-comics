<script>

export default{
    name:"Footer",
    data(){
        return{
            images :[
                {
                    src:"../assets/images/footer-facebook.png"
                },

                {
                    src:"../assets/images/footer-twitter.png"
                },

                {
                    src:"../assets/images/footer-youtube.png"
                },
                {
                    src:"../assets/images/footer-periscope.png"
                },
                {
                    src:"../assets/images/footer-pinterest.png"
                }
            ]
        }
    },
    methods:{
        GetImagePath: function(imgPath){
            return new URL(imgPath, import.meta.url ).href;
        }
    }
}



</script>

<template>
    
    <footer>

        <div class="container">

            <div>
                <h4>SIGN-UP NOW!</h4>
            </div>


            <div class="flex">

                <h3>FOLLOW US</h3>


                <div class="flex margin-left">

                    <div v-for="(image ,i) in images" :key="i" class="box-img">
                        <img :src="GetImagePath(image.src)" alt="">
                    </div>

                </div>

               

            </div>






        </div>

        





    </footer>


    
    
    
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;


footer{
    background-color: #303030;
    height: 100px;
    font-size: 14px;

    .container{
        @include space-between;


        h4{
            color: white;
            padding: 0.8rem;
            border: 2px solid #0b6fcb;
        }


        h3{
            color:#0b6fcb ;
        }


        .box-img{
            padding: 0.5rem;
            height: 45px;
            width: 45px;

        }

        .flex{
            @include align-center;
        }


        .margin-left{

            margin-left: 15px;
            
        }
    }
}







</style>
