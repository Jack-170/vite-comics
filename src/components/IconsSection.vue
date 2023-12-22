<script>
export default{
    name:"IconsSection",

    data (){
        return{
            Icons:[
                {
                    text: "DIGITAL COMICS",
                    src: "../assets/images/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    src:"../assets/images/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    src: "../assets/images/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    src: "../assets/images/buy-comics-shop-locator.png",
                },
                {
                    text: "DC POWER VISA",
                    src: "../assets/images/buy-dc-power-visa.svg",
                },
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
    height: 150px;
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
    width: 50px;
    height: 70px;
}



p{
    color: white;
    @include align-center;
    margin-left:12px;
}




</style>
