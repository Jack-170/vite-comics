<script>
export default{
    name:"HeaderComics",
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
            ]
        }
    }

}
</script>

<template>

    <header>
        
        <div class="container">

            <a href="" class="box-img">
                <img src="../assets/images/dc-logo.png" alt="">
            </a>

           <ul>
                <li v-for="link in links">
                    <a :href="link.url" :class="link.current ? 'active':''">{{link.text}}</a>
                </li>  
           </ul>
  

        </div>
        



    </header>

    
  
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins' as *;

.container{
    @include space-between;

    .box-img{
        height: 70px;
        width: 70px;
    }

    ul{
        list-style-type:none;
        display: flex;

        li a{
            text-decoration: none;
            padding: 1rem;
            color: black;

            &.active,
            &:hover {
                color: #4fadf9; 
                
                border-bottom: 3px solid #4fadf9;
                
            }
        }

    }
}

header{
    height: 100px;
    background-color: white;
}



</style>
