<script>
import HeaderComics from './components/HeaderComics.vue';
import ContentSection from './components/ContentSection.vue';
import IconsSection from './components/IconsSection.vue';
import ListSection from './components/ListSection.vue';
import Footer from './components/Footer.vue';





export default{
    components:{
      HeaderComics,
      ContentSection,
      IconsSection,
      ListSection,
      Footer
    },
    data (){
        return{
            links : [
                { 
                    text: "Characters", 
                    url:"#",
                    current: false
                },
                { 
                    text: "Comics", 
                    url:"#",
                    current: true
                },
                { 
                    text: "Movies", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Tv ", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Games", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Collectibles", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Videos", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Fans", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "News", 
                    url:"#",
                    current: false 
                },
                { 
                    text: "Shop", 
                    url:"#",
                    current: false 
                }
            ],
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
    }
}

</script>

<template>

 <HeaderComics :links="links" />

 <main>

  <ContentSection/>

  <IconsSection :Icons="Icons"/>

  <ListSection/>
  
 </main>

 

 <Footer/>
 
</template>

<style lang="scss">
@use './styles/general.scss' as *;

</style>
